---
title: Comment partager des dossiers entre l'hôte et l'espace de travail MED-V
description: Comment partager des dossiers entre l'hôte et l'espace de travail MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811345"
---
# <span data-ttu-id="67f18-103">Comment partager des dossiers entre l'hôte et l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="67f18-103">How to Share Folders Between the Host and the MED-V Workspace</span></span>


<span data-ttu-id="67f18-104">Vous pouvez partager des dossiers entre l’hôte et l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="67f18-104">You can share folders between the host and the MED-V workspace.</span></span> <span data-ttu-id="67f18-105">Les dossiers partagés peuvent être stockés comme suit:</span><span class="sxs-lookup"><span data-stu-id="67f18-105">The shared folders can be stored on the following:</span></span>

-   <span data-ttu-id="67f18-106">Un ordinateur externe sur le réseau</span><span class="sxs-lookup"><span data-stu-id="67f18-106">An external computer on the network</span></span>

-   <span data-ttu-id="67f18-107">Ordinateur hôte</span><span class="sxs-lookup"><span data-stu-id="67f18-107">The host computer</span></span>

<span data-ttu-id="67f18-108">Les procédures suivantes vous montrent comment partager des dossiers entre l’hôte et l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="67f18-108">The following procedures demonstrate how to share folders between the host and the MED-V workspace.</span></span>

**<span data-ttu-id="67f18-109">Pour partager des dossiers situés sur le réseau</span><span class="sxs-lookup"><span data-stu-id="67f18-109">To share folders located on the network</span></span>**

1.  <span data-ttu-id="67f18-110">Configurez MED-V en mode Bureau complet.</span><span class="sxs-lookup"><span data-stu-id="67f18-110">Configure MED-V in full desktop mode.</span></span>

2.  <span data-ttu-id="67f18-111">Dans gestion MED-V, sous l’onglet réseau, cliquez sur **utiliser une adresse IP différente de celle**de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="67f18-111">In MED-V management, on the Network tab, click **Use different IP address than host (Bridge)**.</span></span>

3.  <span data-ttu-id="67f18-112">Procédez comme suit sur l’ordinateur hôte:</span><span class="sxs-lookup"><span data-stu-id="67f18-112">Do the following on the host computer:</span></span>

    1.  <span data-ttu-id="67f18-113">Dans le panneau de configuration, cliquez sur **afficher l’État et les tâches du réseau**, puis définissez **découverte réseau** sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="67f18-113">In Control Panel, click **View network status and tasks**, and set **Network discovery** to **On**.</span></span>

    2.  <span data-ttu-id="67f18-114">Dans le menu Démarrer, cliquez avec le bouton droit sur **ordinateur**, puis cliquez sur **mapper le lecteur réseau**.</span><span class="sxs-lookup"><span data-stu-id="67f18-114">On the Start menu, right-click **Computer**, and click **Map network drive**.</span></span>

    3.  <span data-ttu-id="67f18-115">Dans la boîte de dialogue **connecter un lecteur réseau** , dans le champ **lecteur** , sélectionnez un lecteur.</span><span class="sxs-lookup"><span data-stu-id="67f18-115">In the **Map Network Drive** dialog box, in the **Drive** field, select a drive.</span></span>

        <span data-ttu-id="67f18-116">**Remarques**  Vérifiez que la même lettre de lecteur n’est pas utilisée sur les deux ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="67f18-116">**Note** Ensure that the same drive letter is not in use on both computers.</span></span>

         

    4.  <span data-ttu-id="67f18-117">Cliquez sur **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="67f18-117">Click **Browse**.</span></span>

    5.  <span data-ttu-id="67f18-118">Dans la boîte de dialogue **Rechercher un dossier** , accédez au lecteur partagé, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="67f18-118">In the **Browse For Folder** dialog box, browse to the shared drive, and click **OK**.</span></span>

    6.  <span data-ttu-id="67f18-119">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="67f18-119">Click **Finish**.</span></span>

4.  <span data-ttu-id="67f18-120">Répétez l’étape 3 dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="67f18-120">Repeat step 3 in the MED-V workspace.</span></span> <span data-ttu-id="67f18-121">Pointez sur le même lecteur que sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="67f18-121">Point to the same drive as on the host computer.</span></span>

**<span data-ttu-id="67f18-122">Pour partager des dossiers situés sur l’hôte</span><span class="sxs-lookup"><span data-stu-id="67f18-122">To share folders located on the host</span></span>**

1.  <span data-ttu-id="67f18-123">Configurez le dossier à partager avec les autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="67f18-123">Configure the folder to be shared with the appropriate permissions.</span></span>

2.  <span data-ttu-id="67f18-124">À partir de l’espace de travail MED-V, accédez à **Mes emplacements réseau** et recherchez le dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="67f18-124">From the MED-V workspace, go to **My network places** and locate the shared folder.</span></span>

3.  <span data-ttu-id="67f18-125">À partir de l’espace de travail MED-V, recherchez le dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="67f18-125">From the MED-V workspace, locate the shared folder.</span></span>

<span data-ttu-id="67f18-126">**Remarques**  Assurez-vous que les ordinateurs d’espace de travail hôte et MED-V se trouvent dans le même domaine ou groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="67f18-126">**Note** Ensure that both the host and MED-V workspace computers are in the same domain or workgroup.</span></span>

 

 

 





