---
title: Suppression du logiciel ou des composants serveur de MBAM
description: Suppression du logiciel ou des composants serveur de MBAM
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810878"
---
# <span data-ttu-id="e2e95-103">Suppression du logiciel ou des composants serveur de MBAM</span><span class="sxs-lookup"><span data-stu-id="e2e95-103">Removing MBAM Server Features or Software</span></span>


<span data-ttu-id="e2e95-104">Ces instructions expliquent comment supprimer des logiciels et des fonctionnalités de Microsoft BitLocker administration et de la surveillance (MBAM).</span><span class="sxs-lookup"><span data-stu-id="e2e95-104">These instructions explain how to remove software and features from Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="e2e95-105">Si vous supprimez les fonctionnalités de MBAM Server, seules les fonctionnalités configurées sont supprimées du serveur et non du logiciel de serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="e2e95-105">If you remove MBAM Server features, only the configured features are removed from the server, not the MBAM Server software.</span></span> <span data-ttu-id="e2e95-106">Si vous supprimez le logiciel serveur MBAM, le logiciel et les fonctionnalités de MBAM Server que vous avez configurées sur ce serveur sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="e2e95-106">If you remove the MBAM Server software, the software and any MBAM Server features that you configured on that server are removed.</span></span>

<span data-ttu-id="e2e95-107">**Remarques**  Pour empêcher la suppression accidentelle de données, MBAM ne propose aucun mécanisme de suppression des bases de données. vous devez le faire manuellement.</span><span class="sxs-lookup"><span data-stu-id="e2e95-107">**Note** To prevent the accidental removal of data, MBAM provides no mechanism for removing the databases; you must do that manually.</span></span>

 

## <a href="" id="bkmk-removeserverfeatures"></a><span data-ttu-id="e2e95-108">Suppression des fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="e2e95-108">Removing MBAM Server features</span></span>


<span data-ttu-id="e2e95-109">Vous pouvez utiliser l’une des méthodes suivantes pour supprimer les fonctionnalités du serveur MBAM que vous avez configurées:</span><span class="sxs-lookup"><span data-stu-id="e2e95-109">You can use either of the following methods to remove MBAM Server features that you have configured:</span></span>

-   <span data-ttu-id="e2e95-110">Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="e2e95-110">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="e2e95-111">Cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2e95-111">Windows PowerShell cmdlets</span></span>

### <span data-ttu-id="e2e95-112">Utilisation de l’Assistant Configuration de MBAM Server pour supprimer des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="e2e95-112">Using the MBAM Server Configuration wizard to remove features</span></span>

<span data-ttu-id="e2e95-113">Suivez ces instructions pour utiliser l’Assistant Configuration de MBAM Server pour supprimer les fonctionnalités du serveur MBAM configurées d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="e2e95-113">Follow these instructions to use the MBAM Server Configuration wizard to remove configured MBAM Server features from a server.</span></span>

**<span data-ttu-id="e2e95-114">Pour supprimer les fonctionnalités d’MBAM à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="e2e95-114">To remove MBAM features by using the wizard</span></span>**

1.  <span data-ttu-id="e2e95-115">Sur le serveur sur lequel vous voulez supprimer des composants, sélectionnez **MBAM Server Configuration** pour ouvrir l’Assistant Configuration.</span><span class="sxs-lookup"><span data-stu-id="e2e95-115">On the server where you want to remove features, select **MBAM Server Configuration** to open the configuration wizard.</span></span>

2.  <span data-ttu-id="e2e95-116">Cliquez sur **Supprimer les fonctionnalités**, sélectionnez les fonctionnalités à supprimer, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e2e95-116">Click **Remove Features**, select the features to remove, and then click **Next**.</span></span> <span data-ttu-id="e2e95-117">Une page de **Résumé** affiche les fonctionnalités que vous avez sélectionnées pour suppression.</span><span class="sxs-lookup"><span data-stu-id="e2e95-117">A **Summary** page displays the features you selected for removal.</span></span>

3.  <span data-ttu-id="e2e95-118">Cliquez sur **supprimer** pour commencer à supprimer les fonctionnalités, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e2e95-118">Click **Remove** to start removing the features, and then click **Close**.</span></span>

### <span data-ttu-id="e2e95-119">Utilisation de Windows PowerShell pour supprimer des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="e2e95-119">Using Windows PowerShell to remove features</span></span>

<span data-ttu-id="e2e95-120">Suivez les étapes ci-dessous pour supprimer les fonctionnalités de MBAM Server à l’aide d’applets de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2e95-120">Use the following steps as a general guide to remove MBAM Server features by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="e2e95-121">Pour supprimer les fonctionnalités d’MBAM à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2e95-121">To remove MBAM features by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="e2e95-122">Avant de supprimer des fonctionnalités, reportez-vous à [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2e95-122">Before removing any features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="e2e95-123">Utilisez les applets de commande suivantes pour supprimer les fonctionnalités du serveur MBAM:</span><span class="sxs-lookup"><span data-stu-id="e2e95-123">Use the following cmdlets to remove MBAM Server features:</span></span>

    -   <span data-ttu-id="e2e95-124">Disable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="e2e95-124">Disable-MbamReport</span></span>

    -   <span data-ttu-id="e2e95-125">Disable-MbamWebApplication</span><span class="sxs-lookup"><span data-stu-id="e2e95-125">Disable-MbamWebApplication</span></span>

    -   <span data-ttu-id="e2e95-126">Disable-MbamCMIntegration</span><span class="sxs-lookup"><span data-stu-id="e2e95-126">Disable-MbamCMIntegration</span></span>

    <span data-ttu-id="e2e95-127">Pour obtenir de l’aide sur les applets de contrôle Windows PowerShell, tapez cmdlet **Get-Help** &lt; *cmdlet* &gt; ou consultez la page Automation de l’application [Microsoft Desktop Optimization avec Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) pour les applets de MBAM Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2e95-127">To get help with Windows PowerShell cmdlets, type **Get-Help** &lt;*cmdlet*&gt; or see the [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) page for the MBAM Windows PowerShell cmdlets.</span></span>

## <span data-ttu-id="e2e95-128">Suppression du logiciel serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="e2e95-128">Removing MBAM Server software</span></span>


<span data-ttu-id="e2e95-129">Procédez comme suit pour supprimer le logiciel serveur MBAM et toutes les fonctionnalités MBAM Server que vous avez configurées sur ce serveur.</span><span class="sxs-lookup"><span data-stu-id="e2e95-129">Use the following steps to remove the MBAM Server software and any MBAM Server features that you configured on that server.</span></span>

**<span data-ttu-id="e2e95-130">Pour supprimer le logiciel serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="e2e95-130">To remove the MBAM Server software</span></span>**

1.  <span data-ttu-id="e2e95-131">Sur le serveur sur lequel vous souhaitez désinstaller le logiciel serveur MBAM, exécutez **MBAMserversetup.exe** pour démarrer l’Assistant de configuration de l’administration et de la surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e2e95-131">On the server where you want to uninstall the MBAM Server software, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="e2e95-132">Sélectionnez **désinstaller**, puis suivez les invites restantes pour terminer le processus de désinstallation du logiciel serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="e2e95-132">Select **Uninstall**, and follow the remaining prompts to complete the process of uninstalling the MBAM Server software.</span></span>



## <span data-ttu-id="e2e95-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2e95-133">Related topics</span></span>


[<span data-ttu-id="e2e95-134">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="e2e95-134">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

 

 

## <span data-ttu-id="e2e95-135">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="e2e95-135">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e2e95-136">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="e2e95-136">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e2e95-137">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e2e95-137">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



