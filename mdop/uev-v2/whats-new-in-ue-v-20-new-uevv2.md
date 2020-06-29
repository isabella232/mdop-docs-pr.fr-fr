---
title: Nouveautés dans UE-V2.0
description: Nouveautés dans UE-V2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810871"
---
# <span data-ttu-id="e87cb-103">Nouveautés dans UE-V2.0</span><span class="sxs-lookup"><span data-stu-id="e87cb-103">What's New in UE-V 2.0</span></span>


<span data-ttu-id="e87cb-104">La virtualisation de l’interface utilisateur de Microsoft (UE-V) 2,0 fournit ces nouvelles fonctionnalités et les fonctionnalités de UE-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="e87cb-104">Microsoft User Experience Virtualization (UE-V) 2.0 provides these new features and functionality compared to UE-V 1.0.</span></span> <span data-ttu-id="e87cb-105">Les [notes de publication de Microsoft User Interface Virtualization (UE-v) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) fournissent des informations supplémentaires sur la version d’UE-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="e87cb-105">The [Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) provide more information about the UE-V 2.0 release.</span></span>

## <span data-ttu-id="e87cb-106">Le cache côté client (CSC) n’est plus requis</span><span class="sxs-lookup"><span data-stu-id="e87cb-106">Client-side cache (CSC) no longer required</span></span>


<span data-ttu-id="e87cb-107">Cette version de UE-V introduit le **fournisseur de synchronisation**, qui remplace l’exigence de la fonctionnalité fichiers en mode hors connexion de Windows pour la prise en charge d’un cache côté client de paramètres.</span><span class="sxs-lookup"><span data-stu-id="e87cb-107">This version of UE-V introduces the **sync provider**, which replaces the requirement for the Windows Offline Files feature to support a client-side cache of settings.</span></span>

<span data-ttu-id="e87cb-108">Considérant que UE-V a utilisé pour synchroniser les paramètres uniquement lorsqu’une application est ouverte, fermée ou lorsque Windows est verrouillé ou déverrouillé, ou à l’ouverture ou à la fermeture de session, le fournisseur de synchronisation...</span><span class="sxs-lookup"><span data-stu-id="e87cb-108">Whereas UE-V used to synchronize settings only when an application opened, closed, or when Windows locked or unlocked, or at logon or logoff, the sync provider also …</span></span>

-   <span data-ttu-id="e87cb-109">Synchronise les paramètres de l’application locale et de Windows hors-bande à l’aide d’un**déclencheur d’événements**</span><span class="sxs-lookup"><span data-stu-id="e87cb-109">Synchronizes local application and Windows settings out-of-band using "**trigger events**"</span></span>

-   <span data-ttu-id="e87cb-110">Utilise une **tâche planifiée** pour synchroniser le package de stockage des paramètres dans tout intervalle que vous choisissez pour les besoins de votre entreprise (toutes les 30 minutes par défaut)</span><span class="sxs-lookup"><span data-stu-id="e87cb-110">Uses a **scheduled task** to sync the settings storage package in any interval you choose for your enterprise requirements (every 30 minutes by default)</span></span>

<span data-ttu-id="e87cb-111">Certaines conditions permettent une synchronisation plus fréquente.</span><span class="sxs-lookup"><span data-stu-id="e87cb-111">Certain conditions provide more frequent synchronization.</span></span>

-   <span data-ttu-id="e87cb-112">Les paramètres sont synchronisés quand l’utilisateur clique sur le bouton **Synchroniser maintenant** dans l’application Centre de paramètres de nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="e87cb-112">Settings synchronize when the user clicks the **Sync Now** button in the new Company Settings Center application.</span></span>

-   <span data-ttu-id="e87cb-113">Le fournisseur de synchronisation peut également démarrer pour une application unique sans attendre la tâche de synchronisation planifiée.</span><span class="sxs-lookup"><span data-stu-id="e87cb-113">The sync provider can also start for a single application without waiting for the scheduled synchronization task.</span></span> <span data-ttu-id="e87cb-114">Par exemple, quand une application est fermée, les modifications apportées aux paramètres sont écrites dans le cache local, et le processus du fournisseur de synchronisation s’exécute de manière asynchrone pour déplacer ces modifications de paramètres vers l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e87cb-114">For example, when an application is closed, any settings changes are written to the local cache, and the sync provider process runs asynchronously to move those new settings changes to the settings storage location.</span></span>

## <span data-ttu-id="e87cb-115">Synchronisation d’applications Windows</span><span class="sxs-lookup"><span data-stu-id="e87cb-115">Windows app synchronization</span></span>


<span data-ttu-id="e87cb-116">Le développeur d’une application Windows peut définir les paramètres, le cas échéant, à synchroniser, et ces paramètres peuvent désormais être capturés et synchronisés avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="e87cb-116">The developer of a Windows app can define which settings, if any, are to be synchronized, and these settings can now be captured and synchronized with UE-V.</span></span>

<span data-ttu-id="e87cb-117">Par défaut, UE-V synchronise les paramètres de nombreux logiciels Windows inclus dans Windows 8 et Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="e87cb-117">By default, UE-V synchronizes the settings of many of the Windows apps included in Windows 8 and Windows 8.1.</span></span> <span data-ttu-id="e87cb-118">Vous pouvez modifier la liste des applications synchronisées avec Windows PowerShell, Windows Management Instrumentation (WMI) ou une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e87cb-118">You can modify the list of synchronized apps with Windows PowerShell, Windows Management Instrumentation (WMI), or Group Policy.</span></span>

<span data-ttu-id="e87cb-119">**Remarques**  UE-V ne synchronise pas les paramètres des applications Windows si les utilisateurs du domaine lient leurs informations d’identification de connexion à leur compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e87cb-119">**Note** UE-V does not synchronize Windows app settings if the domain users link their sign-in credentials to their Microsoft account.</span></span> <span data-ttu-id="e87cb-120">Ce lien permet de synchroniser les paramètres avec Microsoft OneDrive de manière à ce que UE-V ne synchronise que les applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="e87cb-120">This linking synchronizes settings to Microsoft OneDrive so UE-V only synchronizes the desktop applications.</span></span>

 

## <span data-ttu-id="e87cb-121">Liaison de compte Microsoft</span><span class="sxs-lookup"><span data-stu-id="e87cb-121">Microsoft account linking</span></span>


<span data-ttu-id="e87cb-122">La synchronisation des paramètres via OneDrive est une nouveauté de Windows 8 lorsque vous êtes connecté avec un compte Microsoft ou si vous liez votre compte Microsoft à votre compte de domaine.</span><span class="sxs-lookup"><span data-stu-id="e87cb-122">Settings synchronization via OneDrive is new to Windows 8 when you are signed in with a Microsoft account or if you link your Microsoft account to your domain account.</span></span> <span data-ttu-id="e87cb-123">Si un utilisateur du domaine utilise UE-V et s’est connecté à un compte Microsoft, alors...</span><span class="sxs-lookup"><span data-stu-id="e87cb-123">If a domain user uses UE-V and has signed in to a Microsoft account, then…</span></span>

-   <span data-ttu-id="e87cb-124">UE-V ne synchronise que les paramètres des applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="e87cb-124">UE-V only synchronizes settings for desktop applications</span></span>

-   <span data-ttu-id="e87cb-125">Le compte Microsoft gère les paramètres d’application Windows et les paramètres de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="e87cb-125">Microsoft account handles Windows app settings and Windows desktop settings</span></span>

## <span data-ttu-id="e87cb-126">Centre de paramètres de la société</span><span class="sxs-lookup"><span data-stu-id="e87cb-126">Company Settings Center</span></span>


<span data-ttu-id="e87cb-127">Vous pouvez fournir aux utilisateurs un contrôle sur les paramètres qui sont synchronisés par le biais d’une application dans UE-V 2 appelé centre de paramètres de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e87cb-127">You can provide your users with some control over which settings are synchronized through an application in UE-V 2 called Company Settings Center.</span></span> <span data-ttu-id="e87cb-128">Le centre de gestion des paramètres de l’entreprise est installé avec l’agent UE-V, et les utilisateurs peuvent y accéder à partir du panneau de configuration, du menu **Démarrer** ou de l’écran d' **Accueil** , et à partir de l’icône de zone de notification UE-v.</span><span class="sxs-lookup"><span data-stu-id="e87cb-128">Company Settings Center is installed along with the UE-V Agent, and users can access it from Control Panel, the **Start** menu or **Start** screen, and from the UE-V notification area icon.</span></span>

<span data-ttu-id="e87cb-129">Le centre de paramètres de la société affiche les paramètres qui sont synchronisés et permet aux utilisateurs d’afficher l’état de synchronisation d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="e87cb-129">Company Settings Center displays which settings are synchronized and lets users see the synchronization status of UE-V.</span></span> <span data-ttu-id="e87cb-130">Si vous les autorisez, les utilisateurs peuvent utiliser le centre de paramètres d’une entreprise pour sélectionner les paramètres de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e87cb-130">If you let them, users can use Company Settings Center to select which settings to synchronize.</span></span> <span data-ttu-id="e87cb-131">Ils peuvent également cliquer sur le bouton **Synchroniser maintenant** pour synchroniser tous les paramètres immédiatement.</span><span class="sxs-lookup"><span data-stu-id="e87cb-131">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span>






## <span data-ttu-id="e87cb-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e87cb-132">Related topics</span></span>


[<span data-ttu-id="e87cb-133">Prise en main d'UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="e87cb-133">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="e87cb-134">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="e87cb-134">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="e87cb-135">Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0</span><span class="sxs-lookup"><span data-stu-id="e87cb-135">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





