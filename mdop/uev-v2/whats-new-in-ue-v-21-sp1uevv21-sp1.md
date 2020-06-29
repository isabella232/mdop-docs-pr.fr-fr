---
title: Nouveautés dans UE-V2.1SP1
description: Nouveautés dans UE-V2.1SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812348"
---
# <span data-ttu-id="5190a-103">Nouveautés dans UE-V2.1SP1</span><span class="sxs-lookup"><span data-stu-id="5190a-103">What's New in UE-V 2.1 SP1</span></span>


<span data-ttu-id="5190a-104">User performance Virtualization 2,1 SP1 fournit les nouvelles fonctionnalités par rapport à UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="5190a-104">User Experience Virtualization 2.1 SP1 provides these new features and functionality compared to UE-V 2.1.</span></span> <span data-ttu-id="5190a-105">Les [notes de publication de Microsoft User Interface Virtualization (UE-v) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) fournissent des informations supplémentaires sur la version d’UE-v 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="5190a-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) provide more information about the UE-V 2.1 SP1 release.</span></span>

## <span data-ttu-id="5190a-106">Prise en charge de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5190a-106">Support for Windows 10</span></span>


<span data-ttu-id="5190a-107">UE-V 2,1 SP1 ajoute la prise en charge de Windows 10, en plus des logiciels pris en charge dans les versions antérieures d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="5190a-107">UE-V 2.1 SP1 adds support for Windows 10, in addition to the same software that is supported in earlier versions of UE-V.</span></span>

### <span data-ttu-id="5190a-108">Compatibilité avec Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="5190a-108">Compatibility with Microsoft Azure</span></span>

<span data-ttu-id="5190a-109">Windows 10 permet aux utilisateurs d’entreprise de synchroniser les paramètres des applications Windows et les paramètres du système d’exploitation Windows sur Azure plutôt que sur OneDrive.</span><span class="sxs-lookup"><span data-stu-id="5190a-109">Windows 10 lets enterprise users synchronize Windows app settings and Windows operating system settings to Azure instead of to OneDrive.</span></span> <span data-ttu-id="5190a-110">Vous pouvez utiliser la fonctionnalité de synchronisation Windows 10 entreprise conjointement avec UE-V pour les ordinateurs appartenant à un domaine local uniquement.</span><span class="sxs-lookup"><span data-stu-id="5190a-110">You can use the Windows 10 enterprise sync functionality together with UE-V for on-premises domain-joined computers only.</span></span> <span data-ttu-id="5190a-111">Pour activer la coexistence entre Windows 10 et UE-V, vous devez désactiver les modèles UE-V suivants à l’aide de PowerShell sur chaque client ou stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5190a-111">To enable coexistence between Windows 10 and UE-V, you must disable the following UE-V templates using either PowerShell on each client or Group Policy.</span></span>

<span data-ttu-id="5190a-112">Dans stratégie de groupe, sous le nœud Microsoft User performance, configurez les paramètres de stratégie suivants:</span><span class="sxs-lookup"><span data-stu-id="5190a-112">In Group Policy, under the Microsoft User Experience Virtualization node, configure these policy settings:</span></span>

-   <span data-ttu-id="5190a-113">Activer «ne pas synchroniser les applications Windows»</span><span class="sxs-lookup"><span data-stu-id="5190a-113">Enable “Do Not Synchronize Windows Apps”</span></span>

-   <span data-ttu-id="5190a-114">Désactiver «synchroniser les paramètres Windows»</span><span class="sxs-lookup"><span data-stu-id="5190a-114">Disable “Sync Windows Settings”</span></span>

### <span data-ttu-id="5190a-115">Comportement de la synchronisation des paramètres modifié pour la prise en charge de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5190a-115">Settings Synchronization Behavior Changed for Windows 10 Support</span></span>

<span data-ttu-id="5190a-116">UE-V 2,1 SP1 répartir les paramètres de la barre des tâches entre les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5190a-116">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="5190a-117">Toutefois, UE-V ne synchronise pas les paramètres de la barre des tâches entre les appareils et appareils Windows 10 exécutant d’anciens systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5190a-117">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>

<span data-ttu-id="5190a-118">Par ailleurs, UE-V 2,1 SP1 ne synchronise pas les paramètres entre Microsoft Calculator dans Windows 10 et la calculatrice Microsoft dans les systèmes d’exploitation précédents.</span><span class="sxs-lookup"><span data-stu-id="5190a-118">In addition, UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>

## <span data-ttu-id="5190a-119">Prise en charge ajoutée pour les imprimantes réseau itinérantes</span><span class="sxs-lookup"><span data-stu-id="5190a-119">Support Added for Roaming Network Printers</span></span>


<span data-ttu-id="5190a-120">UE-V 2,1 SP1 permet aux imprimantes réseau d’avoir accès aux périphériques de sorte que l’utilisateur ait accès à ses imprimantes réseau lorsqu’il est connecté à un appareil du réseau.</span><span class="sxs-lookup"><span data-stu-id="5190a-120">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="5190a-121">Cela comprend l’itinérance de l’imprimante définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="5190a-121">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="5190a-122">L’itinérance d’imprimantes dans UE-V nécessite l’un des scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="5190a-122">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="5190a-123">Le serveur d’impression peut télécharger le pilote requis lorsqu’il est itinérant vers un nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="5190a-123">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="5190a-124">Le pilote de l’imprimante du réseau errant est préinstallé sur n’importe quel appareil qui a besoin d’accéder à cette imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="5190a-124">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="5190a-125">Le pilote de l’imprimante peut être obtenu à partir de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="5190a-125">The printer driver can be obtained from Windows Update.</span></span>

<span data-ttu-id="5190a-126">**Remarques**  La fonctionnalité d’itinérance d’imprimante UE-V n’effectue **pas** de paramètres d’impression ou de préférences tels que l’impression recto verso.</span><span class="sxs-lookup"><span data-stu-id="5190a-126">**Note** The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>

 

## <span data-ttu-id="5190a-127">Modèle d’emplacement des paramètres d’Office 2013</span><span class="sxs-lookup"><span data-stu-id="5190a-127">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="5190a-128">UE-V 2,1 et 2,1 SP1 incluent le modèle d’emplacement des paramètres Microsoft Office 2013 avec une prise en charge améliorée des signatures Outlook.</span><span class="sxs-lookup"><span data-stu-id="5190a-128">UE-V 2.1 and 2.1 SP1 include the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="5190a-129">Nous avons ajouté la synchronisation des paramètres de signature par défaut pour les courriers électroniques, les réponses et les transferts.</span><span class="sxs-lookup"><span data-stu-id="5190a-129">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="5190a-130">Les clients n’ont plus besoin de choisir les paramètres de signature par défaut.</span><span class="sxs-lookup"><span data-stu-id="5190a-130">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="5190a-131">**Remarques**  Un profil Outlook doit être créé pour tout appareil sur lequel un utilisateur souhaite synchroniser sa signature Outlook.</span><span class="sxs-lookup"><span data-stu-id="5190a-131">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="5190a-132">Si ce n’est pas le cas, l’utilisateur peut en créer un, puis redémarrer Outlook sur cet appareil pour activer la synchronisation des signatures.</span><span class="sxs-lookup"><span data-stu-id="5190a-132">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="5190a-133">Auparavant, UE-V incluait les modèles d’emplacement des paramètres Microsoft Office 2010 qui ont été automatiquement distribués et enregistrés auprès de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="5190a-133">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="5190a-134">UE-V 2,1 utilise Office 365 pour déterminer si les paramètres d’Office 2013 sont itinérants par Office 365.</span><span class="sxs-lookup"><span data-stu-id="5190a-134">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="5190a-135">Si les paramètres sont itinérants par Office 365, ils ne sont pas itinérants par UE-V.</span><span class="sxs-lookup"><span data-stu-id="5190a-135">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="5190a-136">La [vue d’ensemble des paramètres utilisateur et itinérance pour Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) fournit des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5190a-136">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="5190a-137">Pour activer la synchronisation des paramètres avec UE-V 2,1, effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="5190a-137">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="5190a-138">Utiliser une stratégie de groupe pour désactiver la synchronisation d’Office 365</span><span class="sxs-lookup"><span data-stu-id="5190a-138">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="5190a-139">Ne pas activer l’interface de synchronisation Office 365 lors de l’installation d’Office 2013</span><span class="sxs-lookup"><span data-stu-id="5190a-139">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="5190a-140">UE-V 2,1 inclut [les modèles office 2013 et office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="5190a-140">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="5190a-141">Cette version supprime les modèles Office 2007.</span><span class="sxs-lookup"><span data-stu-id="5190a-141">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="5190a-142">Les utilisateurs peuvent toujours utiliser les modèles Office 2007 d’UE-V 2,0 ou une version antérieure et peuvent toujours obtenir les modèles de la Galerie de modèles UE-V située [ici](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="5190a-142">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>






## <span data-ttu-id="5190a-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5190a-143">Related topics</span></span>


[<span data-ttu-id="5190a-144">Prise en main d'UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="5190a-144">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="5190a-145">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="5190a-145">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="5190a-146">Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1SP1</span><span class="sxs-lookup"><span data-stu-id="5190a-146">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





