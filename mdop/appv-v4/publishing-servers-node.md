---
title: Nœud Serveurs de publication
description: Nœud Serveurs de publication
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806450"
---
# <span data-ttu-id="4d776-103">Nœud Serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="4d776-103">Publishing Servers Node</span></span>


<span data-ttu-id="4d776-104">Le nœud **serveurs de publication** se trouve à un niveau sous le nœud **Application Virtualization** dans le volet d' **étendue** de la console de gestion des clients de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="4d776-104">The **Publishing Servers** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="4d776-105">Lorsque vous sélectionnez ce nœud, le volet **résultats** affiche une liste des serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="4d776-105">When you select this node, the **Results** pane displays a list of publishing servers.</span></span>

<span data-ttu-id="4d776-106">Cliquez avec le bouton droit sur le nœud **serveurs de publication** pour afficher un menu contextuel contenant les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="4d776-106">Right-click the **Publishing Servers** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-server"></a>**<span data-ttu-id="4d776-107">Nouveau serveur</span><span class="sxs-lookup"><span data-stu-id="4d776-107">New Server</span></span>**  
<span data-ttu-id="4d776-108">Cet élément de menu affiche l’Assistant Nouveau serveur.</span><span class="sxs-lookup"><span data-stu-id="4d776-108">This menu item displays the New Server Wizard.</span></span> <span data-ttu-id="4d776-109">Cet Assistant comporte deux pages:</span><span class="sxs-lookup"><span data-stu-id="4d776-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="4d776-110">Entrez le nom d’affichage du serveur et le type du serveur:</span><span class="sxs-lookup"><span data-stu-id="4d776-110">Enter a server display name and server type:</span></span>

    -   <span data-ttu-id="4d776-111">**Nom d’affichage**— entrez le nom que vous souhaitez afficher pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="4d776-111">**Display Name**—Enter a name that you want displayed for the server.</span></span> <span data-ttu-id="4d776-112">Ce champ est vide par défaut.</span><span class="sxs-lookup"><span data-stu-id="4d776-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="4d776-113">**Type**— sélectionnez le type de serveur dans la liste déroulante des types de serveurs.</span><span class="sxs-lookup"><span data-stu-id="4d776-113">**Type**—Choose the server type from the drop-down list of server types.</span></span>

2.  <span data-ttu-id="4d776-114">Spécifiez les paramètres de connexion du serveur:</span><span class="sxs-lookup"><span data-stu-id="4d776-114">Specify the connection settings for the server:</span></span>

    -   <span data-ttu-id="4d776-115">**Nom d’hôte**: entrez le nom ou l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="4d776-115">**Host Name**—Enter the name or IP address for the server.</span></span>

    -   <span data-ttu-id="4d776-116">**Port**: entrez une valeur numérique correspondant au numéro de port.</span><span class="sxs-lookup"><span data-stu-id="4d776-116">**Port**—Enter a numeric value that corresponds to the port number.</span></span> <span data-ttu-id="4d776-117">La valeur par défaut est 554 si le type du serveur est «serveur de virtualisation des applications» et 80 si le type du serveur est «serveur HTTP standard».</span><span class="sxs-lookup"><span data-stu-id="4d776-117">The default value is 554 if the server type is "Application Virtualization Server" and 80 if the server type is "Standard HTTP Server."</span></span>

    -   <span data-ttu-id="4d776-118">**Path**: ce champ par défaut est «/» et est en lecture seule lorsque le type du serveur est «serveur de virtualisation des applications» ou «serveur de virtualisation des applications de sécurité améliorée».</span><span class="sxs-lookup"><span data-stu-id="4d776-118">**Path**—This field defaults to "/" and is read-only when the server type is "Application Virtualization Server" or “Enhanced Security Application Virtualization Server”.</span></span> <span data-ttu-id="4d776-119">Lorsque le type du serveur est «standard HTTP Server» ou «serveur HTTP de sécurité améliorée», le champ **path** peut également être modifié.</span><span class="sxs-lookup"><span data-stu-id="4d776-119">When the server type is “Standard HTTP Server” or “Enhanced Security HTTP Server”, the **Path** field is also editable.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="4d776-120">Nouvelle fenêtre à partir de cet emplacement</span><span class="sxs-lookup"><span data-stu-id="4d776-120">New Window from Here</span></span>**  
<span data-ttu-id="4d776-121">Sélectionnez cet élément de menu pour ouvrir une nouvelle console de gestion avec le nœud sélectionné en tant que nœud racine.</span><span class="sxs-lookup"><span data-stu-id="4d776-121">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="4d776-122">Exporter la liste</span><span class="sxs-lookup"><span data-stu-id="4d776-122">Export List</span></span>**  
<span data-ttu-id="4d776-123">Vous pouvez utiliser cet élément de menu pour créer un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="4d776-123">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="4d776-124">Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.</span><span class="sxs-lookup"><span data-stu-id="4d776-124">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="4d776-125">View (Afficher)</span><span class="sxs-lookup"><span data-stu-id="4d776-125">View</span></span>**  
<span data-ttu-id="4d776-126">Cette liste déroulante des éléments de menu vous permet de modifier l’apparence et le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="4d776-126">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="4d776-127">Actualiser</span><span class="sxs-lookup"><span data-stu-id="4d776-127">Refresh</span></span>**  
<span data-ttu-id="4d776-128">Sélectionnez cet élément pour actualiser la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="4d776-128">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="4d776-129">Help</span><span class="sxs-lookup"><span data-stu-id="4d776-129">Help</span></span>**  
<span data-ttu-id="4d776-130">Cet élément affiche le système d’aide pour la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="4d776-130">This item displays the help system for the management console.</span></span>

## <span data-ttu-id="4d776-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d776-131">Related topics</span></span>


[<span data-ttu-id="4d776-132">Volet de résultats Serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="4d776-132">Publishing Servers Results Pane</span></span>](publishing-servers-results-pane.md)

[<span data-ttu-id="4d776-133">Colonnes du volet de résultats Serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="4d776-133">Publishing Servers Results Pane Columns</span></span>](publishing-servers-results-pane-columns.md)

 

 





