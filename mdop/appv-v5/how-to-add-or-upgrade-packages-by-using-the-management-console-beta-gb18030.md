---
title: Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion
description: Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion
author: dansimp
ms.assetid: 4e389d7e-f402-44a7-bc4c-42c2a8440573
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 583ac07168c44c7d0a605b81512ae01a6d979db2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805749"
---
# <span data-ttu-id="fb505-103">Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="fb505-103">How to Add or Upgrade Packages by Using the Management Console</span></span>


<span data-ttu-id="fb505-104">Vous pouvez effectuer la procédure suivante pour ajouter ou mettre à niveau un package vers la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fb505-104">You can the following procedure to add or upgrade a package to the App-V 5.0 Management Console.</span></span> <span data-ttu-id="fb505-105">Pour mettre à niveau un package déjà existant dans la console de gestion, procédez comme suit et importez le package mis à niveau en utilisant le même **nom**de package.</span><span class="sxs-lookup"><span data-stu-id="fb505-105">To upgrade a package that already exists in the Management Console, use the following steps and import the upgraded package using the same package **Name**.</span></span>

**<span data-ttu-id="fb505-106">Pour ajouter un package à la console de gestion</span><span class="sxs-lookup"><span data-stu-id="fb505-106">To add a package to the Management Console</span></span>**

1.  <span data-ttu-id="fb505-107">Cliquez sur l’onglet **packages** dans le volet de navigation de l’écran de la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="fb505-107">Click the **Packages** tab in the navigation pane of the Management Console display.</span></span>

    <span data-ttu-id="fb505-108">La console affiche la liste des packages qui ont été ajoutés au serveur ainsi que des informations d’État sur chaque package.</span><span class="sxs-lookup"><span data-stu-id="fb505-108">The console displays the list of packages that have been added to the server along with status information about each package.</span></span> <span data-ttu-id="fb505-109">La sélection d’un package permet d’afficher des informations détaillées sur le package dans le volet **packages** .</span><span class="sxs-lookup"><span data-stu-id="fb505-109">When a package is selected, detailed information about the package is displayed in the **PACKAGES** pane.</span></span>

    <span data-ttu-id="fb505-110">Cliquez sur la zone de liste déroulante **dissociée** et spécifiez le mode d’affichage des packages dans la console.</span><span class="sxs-lookup"><span data-stu-id="fb505-110">Click the **Ungrouped** drop-down list box and specify how the packages are to be displayed in the console.</span></span> <span data-ttu-id="fb505-111">Vous pouvez également cliquer sur l’en-tête de colonne associé pour trier les packages.</span><span class="sxs-lookup"><span data-stu-id="fb505-111">You can also click the associated column header to sort the packages.</span></span>

2.  <span data-ttu-id="fb505-112">Pour spécifier le package que vous voulez ajouter, cliquez sur **Ajouter ou mettre à niveau des packages**.</span><span class="sxs-lookup"><span data-stu-id="fb505-112">To specify the package you want to add, click **Add or Upgrade Packages**.</span></span>

3.  <span data-ttu-id="fb505-113">Tapez le chemin d’accès complet au package que vous voulez ajouter.</span><span class="sxs-lookup"><span data-stu-id="fb505-113">Type the full path to the package that you want to add.</span></span> <span data-ttu-id="fb505-114">Utilisez le format de chemin d’accès UNC ou HTTP (par exemple, **\\\\servername\\sharename\\foldername\\packagename.AppV** ou), puis **http://server.1234/file.appv** cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="fb505-114">Use the UNC or HTTP path format, for example **\\\\servername\\sharename\\foldername\\packagename.appv** or **http://server.1234/file.appv**, and then click **Add**.</span></span>

    <span data-ttu-id="fb505-115">**Important**  Vous devez sélectionner un package avec l’extension de nom de fichier **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="fb505-115">**Important** You must select a package with the **.appv** file name extension.</span></span>

     

4.  <span data-ttu-id="fb505-116">La page affiche le message d' **état &lt; ajouter &gt; PackageName**.</span><span class="sxs-lookup"><span data-stu-id="fb505-116">The page displays the status message **Adding &lt;Packagename&gt;**.</span></span> <span data-ttu-id="fb505-117">Cliquez sur **importer le statut** pour vérifier l’état d’un package que vous avez importé.</span><span class="sxs-lookup"><span data-stu-id="fb505-117">Click **IMPORT STATUS** to check the status of a package that you have imported.</span></span>

    <span data-ttu-id="fb505-118">Cliquez sur **OK** pour ajouter le package et fermer la page **Ajouter un package** .</span><span class="sxs-lookup"><span data-stu-id="fb505-118">Click **OK** to add the package and close the **Add Package** page.</span></span> <span data-ttu-id="fb505-119">S’il y a eu une erreur lors de l’importation, cliquez sur **Détails** dans la page **importation du package** pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fb505-119">If there was an error during the import, click **Detail** on the **Package Import** page for more information.</span></span> <span data-ttu-id="fb505-120">Le package que vous venez d’ajouter est désormais disponible dans le volet **packages** .</span><span class="sxs-lookup"><span data-stu-id="fb505-120">The newly added package is now available in the **PACKAGES** pane.</span></span>

5.  <span data-ttu-id="fb505-121">Cliquez sur **Fermer** pour fermer la page **Ajouter ou mettre à niveau des packages** .</span><span class="sxs-lookup"><span data-stu-id="fb505-121">Click **Close** to close the **Add or Upgrade Packages** page.</span></span>

    <span data-ttu-id="fb505-122">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="fb505-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="fb505-123">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="fb505-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="fb505-124">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="fb505-124">Got an App-V issue?</span></span>** <span data-ttu-id="fb505-125">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="fb505-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="fb505-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb505-126">Related topics</span></span>


[<span data-ttu-id="fb505-127">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="fb505-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





