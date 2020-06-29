---
title: Procédure pour publier des raccourcis d'application
description: Procédure pour publier des raccourcis d'application
author: dansimp
ms.assetid: fc5efe86-1bbe-438b-b7d8-4f9b815cc58e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eafdb85414a1a6cf3e1072fdc5532bcd04699653
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806869"
---
# <span data-ttu-id="af46f-103">Procédure pour publier des raccourcis d'application</span><span class="sxs-lookup"><span data-stu-id="af46f-103">How to Publish Application Shortcuts</span></span>


<span data-ttu-id="af46f-104">Vous pouvez utiliser la procédure suivante pour publier des raccourcis vers une application directement à partir du volet **résultats** du nœud de l' **application** dans la console de gestion du client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="af46f-104">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="af46f-105">Pour publier des raccourcis d’application</span><span class="sxs-lookup"><span data-stu-id="af46f-105">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="af46f-106">Positionnez le curseur dans le volet **résultats** , cliquez avec le bouton droit sur l’application souhaitée, puis sélectionnez **nouveau raccourci** dans le menu contextuel pour afficher l’assistant nouveau raccourci.</span><span class="sxs-lookup"><span data-stu-id="af46f-106">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="af46f-107">Dans la première page de l’assistant nouveau raccourci, sélectionnez une icône et attribuez un nom au raccourci.</span><span class="sxs-lookup"><span data-stu-id="af46f-107">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="af46f-108">**Icône modifier**: affiche un navigateur d’icônes Windows standard.</span><span class="sxs-lookup"><span data-stu-id="af46f-108">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="af46f-109">Recherchez et sélectionnez l’icône souhaitée.</span><span class="sxs-lookup"><span data-stu-id="af46f-109">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="af46f-110">**Titre du raccourci**— entrez le nom que vous voulez donner au raccourci.</span><span class="sxs-lookup"><span data-stu-id="af46f-110">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="af46f-111">Par défaut, il s’agit du nom existant et de la version de l’application.</span><span class="sxs-lookup"><span data-stu-id="af46f-111">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="af46f-112">Sur la deuxième page de l’Assistant, déterminez l’emplacement du raccourci publié.</span><span class="sxs-lookup"><span data-stu-id="af46f-112">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="af46f-113">**Bureau**: activez cette case à cocher pour publier le raccourci sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="af46f-113">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="af46f-114">**Barre d’outils Lancement rapide**: activez cette case à cocher pour publier le raccourci dans la barre d’outils Lancement rapide.</span><span class="sxs-lookup"><span data-stu-id="af46f-114">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="af46f-115">**Menu Envoyer vers**: activez cette case à cocher pour publier le raccourci dans le menu **Envoyer vers** .</span><span class="sxs-lookup"><span data-stu-id="af46f-115">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="af46f-116">**Programmes dans le menu Démarrer**: lorsque vous activez la case à cocher **menu Démarrer** , ce champ devient actif.</span><span class="sxs-lookup"><span data-stu-id="af46f-116">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="af46f-117">Ne renseignez pas ce champ pour publier le raccourci directement à la racine du dossier programmes ou entrez un nom de dossier ou une hiérarchie (par exemple, «mon \ _Computer applications \\Office»).</span><span class="sxs-lookup"><span data-stu-id="af46f-117">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="af46f-118">Les raccourcis créés de cette manière sont disponibles uniquement pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="af46f-118">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="af46f-119">**Un autre emplacement et un** bouton **Parcourir** : lorsque vous activez la case à cocher **autre emplacement** , ce champ devient actif.</span><span class="sxs-lookup"><span data-stu-id="af46f-119">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="af46f-120">Entrez un emplacement valide sur votre ordinateur ou un chemin d’accès UNC disponible (fichier ou répertoire partagé sur un réseau).</span><span class="sxs-lookup"><span data-stu-id="af46f-120">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="af46f-121">Le bouton **Parcourir** permet d’afficher une boîte de dialogue d' **ouverture de fichier** Windows standard.</span><span class="sxs-lookup"><span data-stu-id="af46f-121">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="af46f-122">Dans la troisième page de l’Assistant, entrez les paramètres de ligne de commande souhaités.</span><span class="sxs-lookup"><span data-stu-id="af46f-122">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="af46f-123">Cliquez sur **Terminer** pour publier les raccourcis et quitter le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="af46f-123">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="af46f-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af46f-124">Related topics</span></span>


[<span data-ttu-id="af46f-125">Procédure pour ajouter une association de types de fichier</span><span class="sxs-lookup"><span data-stu-id="af46f-125">How to Add a File Type Association</span></span>](how-to-add-a-file-type-association.md)

[<span data-ttu-id="af46f-126">Procédure pour ajouter une application</span><span class="sxs-lookup"><span data-stu-id="af46f-126">How to Add an Application</span></span>](how-to-add-an-application.md)

[<span data-ttu-id="af46f-127">Procédure pour supprimer une association de types de fichier</span><span class="sxs-lookup"><span data-stu-id="af46f-127">How to Delete a File Type Association</span></span>](how-to-delete-a-file-type-association.md)

 

 





