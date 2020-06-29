---
title: Procédure pour supprimer un groupe d'applications
description: Procédure pour supprimer un groupe d'applications
author: dansimp
ms.assetid: 3016b373-f5a0-4c82-96e8-e5e7960f0cc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b392fe84f4318cf7f355de0c07e4d6f1f5108ed7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806845"
---
# <span data-ttu-id="b6794-103">Procédure pour supprimer un groupe d'applications</span><span class="sxs-lookup"><span data-stu-id="b6794-103">How to Remove an Application Group</span></span>


<span data-ttu-id="b6794-104">Pour supprimer un groupe d’applications de la console de gestion du serveur d’applications, vous pouvez procéder de deux façons:</span><span class="sxs-lookup"><span data-stu-id="b6794-104">You can use the following procedures to remove an application group in the Application Virtualization Server Management Console in one of two ways:</span></span>

<span data-ttu-id="b6794-105">**Attention**  La suppression d’un groupe avec ses applications entraîne la suppression de ces applications du serveur de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="b6794-105">**Caution** Deleting a group with its applications deletes those applications from the Application Virtualization Management Server.</span></span> <span data-ttu-id="b6794-106">Lorsque vous procédez ainsi, vous devez confirmer la suppression dans une fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="b6794-106">When you try to do this, you must confirm the deletion in a pop-up window.</span></span>

 

**<span data-ttu-id="b6794-107">Pour vider puis supprimer un groupe d’applications</span><span class="sxs-lookup"><span data-stu-id="b6794-107">To empty and then delete an application group</span></span>**

1.  <span data-ttu-id="b6794-108">Dans la console de gestion du serveur d’applications, développez **applications** dans le volet gauche, puis sélectionnez le groupe d' **applications** que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="b6794-108">In the Application Virtualization Server Management Console, expand **Applications** in the left pane and select the **Application** group you want to remove.</span></span>

2.  <span data-ttu-id="b6794-109">Dans le volet droit, sélectionnez les applications et groupes d’applications que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="b6794-109">In the right pane, select the applications and application groups you want to keep.</span></span> <span data-ttu-id="b6794-110">Vous pouvez utiliser les touches **CTRL** et **MAJ** pour sélectionner plusieurs applications et groupes d’applications.</span><span class="sxs-lookup"><span data-stu-id="b6794-110">You can use the **CTRL** and **Shift** keys to select multiple applications and application groups.</span></span>

3.  <span data-ttu-id="b6794-111">Cliquez avec le bouton droit sur les applications sélectionnées, puis sélectionnez **déplacer**.</span><span class="sxs-lookup"><span data-stu-id="b6794-111">Right-click the selected applications, and choose **Move**.</span></span>

4.  <span data-ttu-id="b6794-112">Dans la fenêtre **Sélectionner la cible** , accédez au nouvel emplacement, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6794-112">In the **Select Target** window, navigate to the new location and click **OK**.</span></span> <span data-ttu-id="b6794-113">Répétez cette étape si vous voulez déplacer différentes applications vers plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="b6794-113">Repeat this step if you want to move different applications to more than one group.</span></span>

5.  <span data-ttu-id="b6794-114">Lorsque vous avez terminé de déplacer les applications que vous souhaitez conserver, cliquez avec le bouton droit sur le groupe d’applications et sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="b6794-114">When you finish moving the applications you want to keep, right-click the application group and choose **Delete**.</span></span>

6.  <span data-ttu-id="b6794-115">Cliquez sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="b6794-115">Click **Yes** to confirm.</span></span>

**<span data-ttu-id="b6794-116">Pour supprimer le groupe avec tous ses groupes enfants et ses applications</span><span class="sxs-lookup"><span data-stu-id="b6794-116">To delete the group, with all its child groups and its applications</span></span>**

1.  <span data-ttu-id="b6794-117">Dans la console de gestion de l’application virtualisation du serveur, développez **applications** dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="b6794-117">In the Application Virtualization Server Management Console, expand **Applications** in the left pane.</span></span>

2.  <span data-ttu-id="b6794-118">Cliquez avec le bouton droit sur le groupe d’application que vous voulez supprimer, puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="b6794-118">Right-click the application group you want to remove, and choose **Delete**.</span></span>

3.  <span data-ttu-id="b6794-119">Cliquez sur **Oui** pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="b6794-119">Click **Yes** to confirm.</span></span>

    <span data-ttu-id="b6794-120">**Remarques**  Vous pouvez sélectionner et supprimer plusieurs groupes d’applications simultanément.</span><span class="sxs-lookup"><span data-stu-id="b6794-120">**Note** You can select and remove multiple application groups simultaneously.</span></span> <span data-ttu-id="b6794-121">Dans le volet droit, utilisez les combinaisons de touches **CTRL**+ clic ou **MAJ**+ clic pour sélectionner plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="b6794-121">In the right pane, use the **CTRL**-click or **Shift**-click key combinations to select more than one group.</span></span>

     

## <span data-ttu-id="b6794-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6794-122">Related topics</span></span>


[<span data-ttu-id="b6794-123">Procédure pour gérer des groupes d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b6794-123">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="b6794-124">Procédure pour gérer des applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b6794-124">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





