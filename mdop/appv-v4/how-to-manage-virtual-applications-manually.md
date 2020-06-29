---
title: Procédure pour gérer manuellement des applications virtuelles
description: Procédure pour gérer manuellement des applications virtuelles
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806977"
---
# <span data-ttu-id="ba443-103">Procédure pour gérer manuellement des applications virtuelles</span><span class="sxs-lookup"><span data-stu-id="ba443-103">How to Manage Virtual Applications Manually</span></span>


<span data-ttu-id="ba443-104">Vous pouvez utiliser la console de gestion des clients Application Virtualization (App-V) pour gérer les applications virtuelles dans le client de bureau App-V ou le client App-V pour les services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ba443-104">You can use the Application Virtualization (App-V) Client Management Console to manage virtual applications in the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="ba443-105">Les administrateurs d’applications-V peuvent utiliser les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="ba443-105">App-V administrators can use perform the following tasks:</span></span>

## <span data-ttu-id="ba443-106">Charger ou décharger une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-106">How to Load or Unload an App-V Application</span></span>


<span data-ttu-id="ba443-107">Vous pouvez utiliser les procédures suivantes pour charger ou décharger une application à partir du cache, directement à partir du volet **résultats** du nœud **application** dans la console de gestion du client de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-107">You can use the following procedures to load or unload an application from the cache, directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="ba443-108">Lorsque vous sélectionnez ce nœud, le volet **résultats** affiche une liste des applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-108">When you select this node, the **Results** pane displays a list of applications.</span></span>

<span data-ttu-id="ba443-109">**Remarques**  Lorsque vous chargez ou déchargez un package, toutes les applications du package sont chargées ou supprimées du cache.</span><span class="sxs-lookup"><span data-stu-id="ba443-109">**Note** When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span> <span data-ttu-id="ba443-110">Lors du chargement d’un package, si vous ne disposez pas de suffisamment d’espace dans le cache pour charger les applications, augmentez la taille de cache.</span><span class="sxs-lookup"><span data-stu-id="ba443-110">When loading a package, if you do not have adequate space in cache to load the applications, increase your cache size.</span></span> <span data-ttu-id="ba443-111">Pour plus d’informations sur la taille de cache, voir [modification de la taille de cache et de la désignation de lettre de lecteur](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span><span class="sxs-lookup"><span data-stu-id="ba443-111">For more information about cache size, see [How to Change the Cache Size and the Drive Letter Designation](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span></span>

 

**<span data-ttu-id="ba443-112">Pour charger une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-112">To load an App-V application</span></span>**

1.  <span data-ttu-id="ba443-113">Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **charger** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-113">Move the cursor to the **Results** pane, right-click the desired application, and select **Load** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ba443-114">L’application est automatiquement chargée.</span><span class="sxs-lookup"><span data-stu-id="ba443-114">The application is automatically loaded.</span></span> <span data-ttu-id="ba443-115">Le suivi de l’avancement est effectué dans la colonne intitulé **État du package**.</span><span class="sxs-lookup"><span data-stu-id="ba443-115">The progress is tracked in the column labeled **Package Status**.</span></span> <span data-ttu-id="ba443-116">Vous devez actualiser l’affichage pour voir que le chargement est terminé ou pour voir la progression.</span><span class="sxs-lookup"><span data-stu-id="ba443-116">You must refresh the view to see that the load is complete or to see the progress.</span></span>

**<span data-ttu-id="ba443-117">Pour décharger une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-117">To unload an App-V application</span></span>**

1.  <span data-ttu-id="ba443-118">Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **décharger** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-118">Move the cursor to the **Results** pane, right-click the desired application, and select **Unload** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ba443-119">L’application est automatiquement déchargée et la colonne **État du package** est mise à jour pour refléter la modification.</span><span class="sxs-lookup"><span data-stu-id="ba443-119">The application is automatically unloaded, and the **Package Status** column is updated to reflect the change.</span></span>

## <span data-ttu-id="ba443-120">Comment effacer une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-120">How to clear an App-V application</span></span>


<span data-ttu-id="ba443-121">Vous pouvez effacer une application de la console directement dans le volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-121">You can clear an application from the console directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="ba443-122">Lorsque vous effacez une application, le système supprime les paramètres, raccourcis et associations de type de fichier qui correspondent à l’application et supprime également l’application de la liste des applications de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba443-122">When you clear an application, the system removes the settings, shortcuts, and file type associations that correspond to the application and also removes the application from the user’s list of applications.</span></span>

<span data-ttu-id="ba443-123">**Remarques**  Lorsque vous effacez une application de la console, vous ne pouvez plus utiliser cette application.</span><span class="sxs-lookup"><span data-stu-id="ba443-123">**Note** When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="ba443-124">Toutefois, l’application reste en cache et reste disponible pour les autres utilisateurs du même système.</span><span class="sxs-lookup"><span data-stu-id="ba443-124">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="ba443-125">Après une actualisation de publication, les applications effacées seront de nouveau accessibles.</span><span class="sxs-lookup"><span data-stu-id="ba443-125">After a publishing refresh, the cleared applications will again become available to you.</span></span> <span data-ttu-id="ba443-126">S’il existe plusieurs applications dans un package, celles-ci ne sont pas supprimées tant que toutes les applications n’ont pas été effacées.</span><span class="sxs-lookup"><span data-stu-id="ba443-126">If there are multiple applications in a package, the user's settings are not removed until all of the applications are cleared.</span></span>

 

**<span data-ttu-id="ba443-127">Pour effacer une application de la console</span><span class="sxs-lookup"><span data-stu-id="ba443-127">To clear an application from the console</span></span>**

1.  <span data-ttu-id="ba443-128">Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **Effacer** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-128">Move the cursor to the **Results** pane, right-click the desired application, and select **Clear** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ba443-129">Dans l’invite de confirmation, cliquez sur **Oui** pour supprimer l’application ou cliquez sur **non** pour annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="ba443-129">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="ba443-130">Comment réparer une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-130">How to Repair an App-V application</span></span>


<span data-ttu-id="ba443-131">Pour réparer une application sélectionnée, vous pouvez effectuer la procédure suivante directement à partir du volet **résultats** du nœud **application** dans la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-131">To repair a selected application, you can perform the following procedure directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="ba443-132">Lorsque vous réparez une application, vous supprimez les paramètres utilisateur personnalisés et restaurez les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="ba443-132">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="ba443-133">Cette action ne modifie pas ou ne supprime aucun raccourci ou association de type de fichier, et ne supprime pas l’application du cache.</span><span class="sxs-lookup"><span data-stu-id="ba443-133">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

**<span data-ttu-id="ba443-134">Pour réparer une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-134">To repair an App-V application</span></span>**

1.  <span data-ttu-id="ba443-135">Déplacer le curseur dans le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ba443-135">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="ba443-136">Cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **réparer** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-136">Right-click the desired application, and select **Repair** from the pop-up menu.</span></span>

3.  <span data-ttu-id="ba443-137">Dans l’invite de confirmation, cliquez sur **Oui** pour réparer l’application ou sur **non** pour annuler.</span><span class="sxs-lookup"><span data-stu-id="ba443-137">At the confirmation prompt, click **Yes** to repair the application or **No** to cancel.</span></span>

## <span data-ttu-id="ba443-138">Comment importer une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-138">How to import an App-V application</span></span>


<span data-ttu-id="ba443-139">Vous pouvez utiliser la procédure suivante pour importer une application dans le cache directement à partir du volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-139">You can use the following procedure to import an application into the cache directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="ba443-140">Pour importer une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-140">To import an App-V application</span></span>**

1.  <span data-ttu-id="ba443-141">Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **Importer** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-141">Move the cursor to the **Results** pane, right-click the desired application, and select **Import** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ba443-142">Dans la fenêtre **Parcourir** , accédez à l’emplacement du fichier de package de l’application voulue, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba443-142">From the **Browse** window, navigate to the location of the package file for the desired application, and then click **OK**.</span></span>

    <span data-ttu-id="ba443-143">**Remarques**  Si vous avez déjà configuré un chemin de recherche d’importation ou si le fichier SFT figure dans le même chemin que la dernière importation réussie, l’étape 2 n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ba443-143">**Note** If you have already configured an import search path or if the SFT file is in the same path as the last successful import, step 2 is not required.</span></span>

     

## <span data-ttu-id="ba443-144">Verrouiller ou déverrouiller une application App-V</span><span class="sxs-lookup"><span data-stu-id="ba443-144">How to lock or unlock an App-V application</span></span>


<span data-ttu-id="ba443-145">Vous pouvez utiliser les procédures suivantes pour verrouiller ou déverrouiller n’importe quelle application dans le cache du client de bureau de la virtualisation de l’application ou le client pour les services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ba443-145">You can use the following procedures to lock or unlock any application in the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services (formerly Terminal Services) cache.</span></span> <span data-ttu-id="ba443-146">Une application verrouillée ne peut pas être supprimée du cache pour libérer de l’espace pour les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-146">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="ba443-147">Pour supprimer une application verrouillée du cache du client de bureau de la virtualisation des applications ou du client du cache des services Bureau à distance, vous devez d’abord la déverrouiller.</span><span class="sxs-lookup"><span data-stu-id="ba443-147">To remove a locked application from the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services cache, you must first unlock it.</span></span>

**<span data-ttu-id="ba443-148">Pour verrouiller une application</span><span class="sxs-lookup"><span data-stu-id="ba443-148">To lock an application</span></span>**

1.  <span data-ttu-id="ba443-149">Déplacer le curseur dans le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ba443-149">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="ba443-150">Cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **Verrouiller** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-150">Right-click the desired application, and select **Lock** from the pop-up menu.</span></span> <span data-ttu-id="ba443-151">L’application sélectionnée est verrouillée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="ba443-151">The selected application is locked in the cache.</span></span>

**<span data-ttu-id="ba443-152">Pour déverrouiller une application</span><span class="sxs-lookup"><span data-stu-id="ba443-152">To unlock an application</span></span>**

1.  <span data-ttu-id="ba443-153">Déplacer le curseur dans le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ba443-153">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="ba443-154">Cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **déverrouiller** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-154">Right-click the desired application, and select **Unlock** from the pop-up menu.</span></span> <span data-ttu-id="ba443-155">L’application sélectionnée est déverrouillée dans le cache et peut être supprimée.</span><span class="sxs-lookup"><span data-stu-id="ba443-155">The selected application is unlocked in the cache and can be removed.</span></span>

## <span data-ttu-id="ba443-156">Comment supprimer une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-156">How to delete an App-V application</span></span>


<span data-ttu-id="ba443-157">Lorsque vous sélectionnez le nœud d' **application** dans la console de gestion du client de virtualisation des applications, le volet **résultats** affiche une liste d’applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-157">When you select the **Application** node in the Application Virtualization Client Management Console, the **Results** pane displays a list of applications.</span></span> <span data-ttu-id="ba443-158">Vous pouvez utiliser la procédure suivante pour supprimer une application du volet **résultats** , qui supprime également l’application du cache.</span><span class="sxs-lookup"><span data-stu-id="ba443-158">You can use the following procedure to delete an application from the **Results** pane, which also removes the application from the cache.</span></span>

<span data-ttu-id="ba443-159">**Remarques**  Lorsque vous supprimez une application, l’application sélectionnée ne sera plus disponible pour les utilisateurs de ce client.</span><span class="sxs-lookup"><span data-stu-id="ba443-159">**Note** When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="ba443-160">Les raccourcis et les associations de types de fichiers sont masqués et l’application est supprimée du cache.</span><span class="sxs-lookup"><span data-stu-id="ba443-160">Shortcuts and file type associations are hidden, and the application is deleted from cache.</span></span> <span data-ttu-id="ba443-161">Toutefois, si une autre application fait référence à des données du cache du système de fichiers pour l’application sélectionnée, ces éléments ne seront pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="ba443-161">However, if another application refers to data in the file system cache data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="ba443-162">Après une actualisation de publication, les applications supprimées vous sont à nouveau accessibles.</span><span class="sxs-lookup"><span data-stu-id="ba443-162">After a publishing refresh, the deleted applications will again become available to you.</span></span>

 

**<span data-ttu-id="ba443-163">Pour supprimer une application</span><span class="sxs-lookup"><span data-stu-id="ba443-163">To delete an application</span></span>**

1.  <span data-ttu-id="ba443-164">Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **supprimer** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-164">Move the cursor to the **Results** pane, right-click the desired application, and select **Delete** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ba443-165">Dans l’invite de confirmation, cliquez sur **Oui** pour supprimer l’application ou cliquez sur **non** pour annuler l’opération.</span><span class="sxs-lookup"><span data-stu-id="ba443-165">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="ba443-166">Comment modifier l’icône d’une application application V</span><span class="sxs-lookup"><span data-stu-id="ba443-166">How to change an App-V application icon</span></span>


<span data-ttu-id="ba443-167">Vous pouvez utiliser la procédure suivante pour modifier une icône associée à l’application sélectionnée directement dans le volet **résultats** du nœud **application** de la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-167">You can use the following procedure to change an icon associated with the selected application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="ba443-168">Pour modifier l’icône d’une application</span><span class="sxs-lookup"><span data-stu-id="ba443-168">To change an application icon</span></span>**

1.  <span data-ttu-id="ba443-169">Positionnez le curseur dans le volet **résultats** , puis cliquez avec le bouton droit sur l’application de votre choix.</span><span class="sxs-lookup"><span data-stu-id="ba443-169">Move the cursor to the **Results** pane, and right-click the desired application.</span></span>

2.  <span data-ttu-id="ba443-170">Sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ba443-170">Select **Properties**.</span></span>

3.  <span data-ttu-id="ba443-171">Dans l’onglet **général** , cliquez sur **modifier l’icône**.</span><span class="sxs-lookup"><span data-stu-id="ba443-171">On the **General** tab, click **Change Icon**.</span></span>

4.  <span data-ttu-id="ba443-172">Sélectionnez l’icône souhaitée ou naviguez jusqu’à un autre emplacement pour sélectionner l’icône.</span><span class="sxs-lookup"><span data-stu-id="ba443-172">Select the desired icon, or browse to another location to select the icon.</span></span> <span data-ttu-id="ba443-173">Après avoir sélectionné l’icône, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba443-173">After you've selected the icon, click **OK**.</span></span> <span data-ttu-id="ba443-174">La nouvelle icône s’affiche dans le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ba443-174">The new icon appears in the **Results** pane.</span></span>

## <span data-ttu-id="ba443-175">Comment ajouter une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-175">How to add an App-V application</span></span>


<span data-ttu-id="ba443-176">Vous pouvez utiliser la procédure suivante pour ajouter une application directement à partir du volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-176">You can use the following procedure to add an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="ba443-177">Pour ajouter une application</span><span class="sxs-lookup"><span data-stu-id="ba443-177">To add an application</span></span>**

1.  <span data-ttu-id="ba443-178">Dans le volet **résultats** , cliquez avec le bouton droit et sélectionnez **nouvelle application** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-178">In the **Results** pane, right-click and select **New Application** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ba443-179">Dans la page de l’Assistant, vous pouvez effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="ba443-179">On the wizard page, you can perform the following tasks:</span></span>

    1.  <span data-ttu-id="ba443-180">**Icône modifier**: affiche un navigateur d’icônes Windows standard.</span><span class="sxs-lookup"><span data-stu-id="ba443-180">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="ba443-181">Recherchez et sélectionnez l’icône souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ba443-181">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="ba443-182">**URL ou chemin d’accès au fichier OSD**: entrez un chemin d’accès absolu local, un chemin d’accès UNC complet (fichier ou répertoire partagé sur un réseau), ou une URL http.</span><span class="sxs-lookup"><span data-stu-id="ba443-182">**OSD File Path or URL**—Enter a local absolute path, a full UNC path (shared file or directory on a network), or an HTTP URL.</span></span>

    3.  <span data-ttu-id="ba443-183">**(Bouton Parcourir l’OSD)**: affiche la boîte de dialogue **ouvrir un fichier** Windows standard.</span><span class="sxs-lookup"><span data-stu-id="ba443-183">**(OSD browse button)**—Displays the standard Windows **Open File** dialog box.</span></span> <span data-ttu-id="ba443-184">Recherchez le fichier souhaité.</span><span class="sxs-lookup"><span data-stu-id="ba443-184">Browse to find the desired file.</span></span>

3.  <span data-ttu-id="ba443-185">Cliquez sur **Terminer** pour ajouter l’application au volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ba443-185">Click **Finish** to add the application to the **Results** pane.</span></span>

## <span data-ttu-id="ba443-186">Publier le raccourci d’une application application V</span><span class="sxs-lookup"><span data-stu-id="ba443-186">How to publish an App-V application shortcut</span></span>


<span data-ttu-id="ba443-187">Vous pouvez utiliser la procédure suivante pour publier des raccourcis vers une application directement à partir du volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-187">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="ba443-188">Pour publier des raccourcis d’application</span><span class="sxs-lookup"><span data-stu-id="ba443-188">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="ba443-189">Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **nouveau raccourci** dans le menu contextuel pour afficher l’assistant nouveau raccourci.</span><span class="sxs-lookup"><span data-stu-id="ba443-189">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="ba443-190">Dans la première page de l’assistant nouveau raccourci, sélectionnez une icône et attribuez un nom au raccourci.</span><span class="sxs-lookup"><span data-stu-id="ba443-190">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="ba443-191">**Icône modifier**: affiche un navigateur d’icônes Windows standard.</span><span class="sxs-lookup"><span data-stu-id="ba443-191">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="ba443-192">Recherchez et sélectionnez l’icône souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ba443-192">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="ba443-193">**Titre du raccourci**— entrez le nom que vous voulez donner au raccourci.</span><span class="sxs-lookup"><span data-stu-id="ba443-193">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="ba443-194">Par défaut, il s’agit du nom existant et de la version de l’application.</span><span class="sxs-lookup"><span data-stu-id="ba443-194">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="ba443-195">Sur la deuxième page de l’Assistant, déterminez l’emplacement du raccourci publié.</span><span class="sxs-lookup"><span data-stu-id="ba443-195">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="ba443-196">**Bureau**: activez cette case à cocher pour publier le raccourci sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="ba443-196">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="ba443-197">**Barre d’outils Lancement rapide**: activez cette case à cocher pour publier le raccourci dans la barre d’outils Lancement rapide.</span><span class="sxs-lookup"><span data-stu-id="ba443-197">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="ba443-198">**Menu Envoyer vers**: activez cette case à cocher pour publier le raccourci dans le menu **Envoyer vers** .</span><span class="sxs-lookup"><span data-stu-id="ba443-198">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="ba443-199">**Programmes dans le menu Démarrer**: lorsque vous activez la case à cocher **menu Démarrer** , ce champ devient actif.</span><span class="sxs-lookup"><span data-stu-id="ba443-199">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="ba443-200">Ne renseignez pas ce champ pour publier le raccourci directement à la racine du dossier programmes ou entrez un nom de dossier ou une hiérarchie (par exemple, «mon \ _Computer applications \\Office»).</span><span class="sxs-lookup"><span data-stu-id="ba443-200">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="ba443-201">Les raccourcis créés de cette manière sont disponibles uniquement pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-201">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="ba443-202">**Un autre emplacement et un** bouton **Parcourir** : lorsque vous activez la case à cocher **autre emplacement** , ce champ devient actif.</span><span class="sxs-lookup"><span data-stu-id="ba443-202">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="ba443-203">Entrez un emplacement valide sur votre ordinateur ou un chemin d’accès UNC disponible (fichier ou répertoire partagé sur un réseau).</span><span class="sxs-lookup"><span data-stu-id="ba443-203">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="ba443-204">Le bouton **Parcourir** permet d’afficher une boîte de dialogue d' **ouverture de fichier** Windows standard.</span><span class="sxs-lookup"><span data-stu-id="ba443-204">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="ba443-205">Dans la troisième page de l’Assistant, entrez les paramètres de ligne de commande souhaités.</span><span class="sxs-lookup"><span data-stu-id="ba443-205">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="ba443-206">Cliquez sur **Terminer** pour publier les raccourcis et quitter le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ba443-206">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="ba443-207">Comment ajouter une association de type de fichier pour une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-207">How to add a file type association for an App-V application</span></span>


<span data-ttu-id="ba443-208">Vous pouvez utiliser la procédure suivante pour ajouter une association de type de fichier à l’aide du nœud **type de fichier** dans la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="ba443-208">You can use the following procedure to add a file type association, using the **File Type Associations** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="ba443-209">Pour ajouter une association de type de fichier</span><span class="sxs-lookup"><span data-stu-id="ba443-209">To add a file type association</span></span>**

1.  <span data-ttu-id="ba443-210">Cliquez avec le bouton droit sur le nœud **type de fichier** , puis sélectionnez **nouvelle association** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba443-210">Right-click the **File Type Associations** node, and select **New Association** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ba443-211">Terminez la première étape de la boîte de dialogue en complétant les informations suivantes, puis cliquez sur **suivant**:</span><span class="sxs-lookup"><span data-stu-id="ba443-211">Complete the first step of the dialog box by completing the following information, and then click **Next**:</span></span>

    1.  <span data-ttu-id="ba443-212">**Extension**— entrez une nouvelle extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="ba443-212">**Extension**—Enter a new file name extension.</span></span> <span data-ttu-id="ba443-213">Ce champ est vide par défaut.</span><span class="sxs-lookup"><span data-stu-id="ba443-213">This field is blank by default.</span></span>

    2.  <span data-ttu-id="ba443-214">**Créer un nouveau type de fichier à l’aide de cette description**: sélectionnez cette case d’option pour entrer une nouvelle description de type de fichier dans le champ actif.</span><span class="sxs-lookup"><span data-stu-id="ba443-214">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="ba443-215">Ce bouton est sélectionné par défaut et le champ actif est vide.</span><span class="sxs-lookup"><span data-stu-id="ba443-215">This button is selected by default, and the active field is blank.</span></span>

    3.  <span data-ttu-id="ba443-216">**Appliquer ce type de fichier à tous les utilisateurs**: activez cette case à cocher si vous voulez que cette association soit globale pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ba443-216">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="ba443-217">Par défaut, cette option est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ba443-217">By default, this box is cleared.</span></span>

    4.  <span data-ttu-id="ba443-218">**Lier cette extension avec un type de fichier existant**: sélectionnez cette case d’option pour associer l’extension au type de fichier existant.</span><span class="sxs-lookup"><span data-stu-id="ba443-218">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="ba443-219">Sélectionnez un type de fichier dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ba443-219">Pick a file type from the drop-down list.</span></span> <span data-ttu-id="ba443-220">Lorsque vous sélectionnez cette option, l’option **suivant** est remplacée par **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ba443-220">When you choose this option, **Next** is changed to **Finish**.</span></span>

3.  <span data-ttu-id="ba443-221">Terminez la deuxième étape de la boîte de dialogue en complétant les informations suivantes, puis cliquez sur **Terminer** pour revenir à la console de gestion du client:</span><span class="sxs-lookup"><span data-stu-id="ba443-221">Complete the second step of the dialog box by completing the following information, and then click **Finish** to return to the Client Management Console:</span></span>

    1.  <span data-ttu-id="ba443-222">**Changer d’icône**: cliquez sur ce bouton pour modifier l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="ba443-222">**Change Icon**—Click this button to change the application icon.</span></span> <span data-ttu-id="ba443-223">Sélectionnez l’une des icônes disponibles ou accédez à un nouvel emplacement, puis sélectionnez une icône.</span><span class="sxs-lookup"><span data-stu-id="ba443-223">Select one of the available icons, or browse to a new location and select an icon.</span></span>

    2.  <span data-ttu-id="ba443-224">**Ouvrir des fichiers avec l’application sélectionnée**: sélectionnez cette case d’option pour ouvrir le fichier avec une application existante.</span><span class="sxs-lookup"><span data-stu-id="ba443-224">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="ba443-225">Dans la liste déroulante des applications disponibles, choisissez une application.</span><span class="sxs-lookup"><span data-stu-id="ba443-225">Choose an application from the drop-down list of available applications.</span></span>

    3.  <span data-ttu-id="ba443-226">**Ouvrez le fichier avec l’Association décrite dans ce fichier OSD**, puis sélectionnez cette case d’option pour spécifier un fichier d’OSD (Open Software Descriptor) qui détermine l’application utilisée pour ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="ba443-226">**Open file with the association described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="ba443-227">Utilisez le bouton Parcourir pour sélectionner un emplacement existant ou entrez un chemin d’accès ou une URL au format HTTP dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="ba443-227">Use the browse button to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

## <span data-ttu-id="ba443-228">Comment supprimer une association de type de fichier pour une application application-V</span><span class="sxs-lookup"><span data-stu-id="ba443-228">How to delete a file type association for an App-V application</span></span>


<span data-ttu-id="ba443-229">Vous pouvez utiliser la procédure suivante pour supprimer une association de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="ba443-229">You can use the following procedure to delete a file type association.</span></span> <span data-ttu-id="ba443-230">Le nœud de **type de fichier** est un niveau sous le nœud **Application Virtualization** dans le volet de l' **étendue** .</span><span class="sxs-lookup"><span data-stu-id="ba443-230">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane.</span></span> <span data-ttu-id="ba443-231">Lorsque vous sélectionnez ce nœud, le volet **résultats** affiche une liste des associations de types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ba443-231">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

**<span data-ttu-id="ba443-232">Pour supprimer une association de type de fichier</span><span class="sxs-lookup"><span data-stu-id="ba443-232">To remove a file type association</span></span>**

1.  <span data-ttu-id="ba443-233">Dans le volet **résultats** , cliquez avec le bouton droit sur l’extension de l’Association de type de fichier que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="ba443-233">In the **Results** pane, right-click the extension of the file type association you want to delete.</span></span>

2.  <span data-ttu-id="ba443-234">Dans le menu contextuel, sélectionnez **supprimer** .</span><span class="sxs-lookup"><span data-stu-id="ba443-234">Select **Delete** from the pop-up menu.</span></span>

3.  <span data-ttu-id="ba443-235">Cliquez sur **Oui** pour supprimer l’Association ou cliquez sur **non** pour revenir au volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ba443-235">Click **Yes** to delete the association, or click **No** to return to the **Results** pane.</span></span>

## <span data-ttu-id="ba443-236">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba443-236">Related topics</span></span>


[<span data-ttu-id="ba443-237">Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="ba443-237">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





