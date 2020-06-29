---
title: Nœud Stratégies du fournisseur
description: Nœud Stratégies du fournisseur
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806465"
---
# <span data-ttu-id="db612-103">Nœud Stratégies du fournisseur</span><span class="sxs-lookup"><span data-stu-id="db612-103">Provider Policies Node</span></span>


<span data-ttu-id="db612-104">Le nœud **stratégies du fournisseur** est un niveau sous le nœud système de virtualisation des applications dans le volet de l' **étendue** de la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="db612-104">The **Provider Policies** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="db612-105">Lorsque vous sélectionnez ce nœud, le volet **résultats** affiche une liste des stratégies du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="db612-105">When you select this node, the **Results** pane displays a list of provider policies.</span></span> <span data-ttu-id="db612-106">Cliquez avec le bouton droit sur le nœud **stratégies du fournisseur** pour afficher un menu contextuel contenant les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="db612-106">Right-click the **Provider Policies** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-provider-policy"></a>**<span data-ttu-id="db612-107">Nouvelle stratégie de fournisseur</span><span class="sxs-lookup"><span data-stu-id="db612-107">New Provider Policy</span></span>**  
<span data-ttu-id="db612-108">Affiche l’Assistant Nouvelle stratégie de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="db612-108">Displays the New Provider Policy Wizard.</span></span> <span data-ttu-id="db612-109">Cet Assistant comprend les pages suivantes:</span><span class="sxs-lookup"><span data-stu-id="db612-109">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="db612-110">Entrez un nom dans le champ nom de la **stratégie du fournisseur** .</span><span class="sxs-lookup"><span data-stu-id="db612-110">Enter a name in the **Provider Policy Name** field.</span></span> <span data-ttu-id="db612-111">Si vous le souhaitez, activez la case à cocher **gérer le Bureau du client à l’aide de la console de gestion** .</span><span class="sxs-lookup"><span data-stu-id="db612-111">Select the **Manage client desktop using the Management Console** check box if you want that capability.</span></span> <span data-ttu-id="db612-112">Activez l’une ou les deux cases à cocher suivantes si vous souhaitez utiliser la fonctionnalité associée:</span><span class="sxs-lookup"><span data-stu-id="db612-112">Select one or both of the following check boxes if you want the associated functionality:</span></span>

    -   **<span data-ttu-id="db612-113">Actualiser la configuration de publication lors de la connexion d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="db612-113">Refresh publishing configuration when a user logs in</span></span>**

    -   <span data-ttu-id="db612-114">**Actualiser la configuration chaque**.</span><span class="sxs-lookup"><span data-stu-id="db612-114">**Refresh configuration every**.</span></span> <span data-ttu-id="db612-115">Après avoir sélectionné cette option, entrez un nombre et sélectionnez l’unité dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="db612-115">After selecting this option, enter a number and select the unit from the drop-down menu.</span></span> <span data-ttu-id="db612-116">Plage d’entrées valides d’un minimum de **30 minutes** à un maximum de **999 jours**.</span><span class="sxs-lookup"><span data-stu-id="db612-116">Valid entries range from a minimum of **30 minutes** to a maximum of **999 days**.</span></span>

2.  <span data-ttu-id="db612-117">Cliquez sur **Ajouter** ou **supprimer** pour ajouter ou supprimer une affectation de groupe.</span><span class="sxs-lookup"><span data-stu-id="db612-117">Click **Add** or **Remove** to add or remove a group assignment.</span></span> <span data-ttu-id="db612-118">Utilisez la boîte de dialogue de **navigation Windows** standard pour rechercher un groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="db612-118">Use the standard **Windows Browse** dialog box to find a user group.</span></span>

3.  <span data-ttu-id="db612-119">Activez une des cases à cocher suivantes dans la boîte de dialogue **configuration du fournisseur de pipeline** pour activer la fonctionnalité associée:</span><span class="sxs-lookup"><span data-stu-id="db612-119">Select one of the following check boxes on the **Provider Pipeline Configuration** dialog box to enable the associated feature:</span></span>

    -   <span data-ttu-id="db612-120">**Authentification**: sélectionnez le type d’authentification dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="db612-120">**Authentication**—Select the type of authentication from the drop-down list.</span></span>

    -   **<span data-ttu-id="db612-121">Appliquer les paramètres d’autorisation d’accès</span><span class="sxs-lookup"><span data-stu-id="db612-121">Enforce Access Permission Settings</span></span>**

    -   **<span data-ttu-id="db612-122">Journalisation des informations d’utilisation</span><span class="sxs-lookup"><span data-stu-id="db612-122">Log Usage Information</span></span>**

    -   <span data-ttu-id="db612-123">Gestion des **licences**: sélectionnez un modèle d’application dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="db612-123">**Licensing**—Select an enforcement scheme from the drop-down list.</span></span>

4.  <span data-ttu-id="db612-124">Cliquez sur **Terminer** pour ajouter la nouvelle stratégie de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="db612-124">Click **Finish** to add the new provider policy.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="db612-125">View (Afficher)</span><span class="sxs-lookup"><span data-stu-id="db612-125">View</span></span>**  
<span data-ttu-id="db612-126">Change l’aspect et le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="db612-126">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="db612-127">Nouvelle fenêtre à partir de cet emplacement</span><span class="sxs-lookup"><span data-stu-id="db612-127">New Window from Here</span></span>**  
<span data-ttu-id="db612-128">Ouvre une nouvelle console de gestion avec le nœud sélectionné en tant que nœud racine.</span><span class="sxs-lookup"><span data-stu-id="db612-128">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="db612-129">Actualiser</span><span class="sxs-lookup"><span data-stu-id="db612-129">Refresh</span></span>**  
<span data-ttu-id="db612-130">Actualise l’affichage du serveur.</span><span class="sxs-lookup"><span data-stu-id="db612-130">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="db612-131">Exporter la liste</span><span class="sxs-lookup"><span data-stu-id="db612-131">Export List</span></span>**  
<span data-ttu-id="db612-132">Crée un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="db612-132">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="db612-133">Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.</span><span class="sxs-lookup"><span data-stu-id="db612-133">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="db612-134">Help</span><span class="sxs-lookup"><span data-stu-id="db612-134">Help</span></span>**  
<span data-ttu-id="db612-135">Affiche le système d’aide pour la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="db612-135">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="db612-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db612-136">Related topics</span></span>


[<span data-ttu-id="db612-137">Server Management Console: nœud Stratégies du fournisseur</span><span class="sxs-lookup"><span data-stu-id="db612-137">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





