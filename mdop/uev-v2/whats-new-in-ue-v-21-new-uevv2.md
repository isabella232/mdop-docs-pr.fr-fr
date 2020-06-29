---
title: Nouveautés dans UE-V2.1
description: Nouveautés dans UE-V2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811651"
---
# <span data-ttu-id="6a3fd-103">Nouveautés dans UE-V2.1</span><span class="sxs-lookup"><span data-stu-id="6a3fd-103">What's New in UE-V 2.1</span></span>


<span data-ttu-id="6a3fd-104">La virtualisation de l’utilisation des utilisateurs 2,1 fournit les nouvelles fonctionnalités par rapport à UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-104">User Experience Virtualization 2.1 provides these new features and functionality compared to UE-V 2.0.</span></span> <span data-ttu-id="6a3fd-105">Les [notes de publication de Microsoft User Interface Virtualization (UE-v) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) fournissent des informations supplémentaires sur la version d’UE-v 2,1.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) provide more information about the UE-V 2.1 release.</span></span>

## <span data-ttu-id="6a3fd-106">Modèle d’emplacement des paramètres d’Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a3fd-106">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="6a3fd-107">UE-V 2,1 inclut le modèle d’emplacement des paramètres Microsoft Office 2013 avec une prise en charge améliorée des signatures Outlook.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-107">UE-V 2.1 includes the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="6a3fd-108">Dans UE-V 2,1, les données de signature sont synchronisées entre les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-108">In UE-V 2.1, the signature data synchronizes between user devices.</span></span> <span data-ttu-id="6a3fd-109">Nous avons ajouté la synchronisation des paramètres de signature par défaut pour les courriers électroniques, les réponses et les transferts.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-109">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="6a3fd-110">Les clients n’ont plus besoin de choisir les paramètres de signature par défaut.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-110">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="6a3fd-111">**Remarques**  Un profil Outlook doit être créé pour tout appareil sur lequel un utilisateur souhaite synchroniser sa signature Outlook.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-111">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="6a3fd-112">Si ce n’est pas le cas, l’utilisateur peut en créer un, puis redémarrer Outlook sur cet appareil pour activer la synchronisation des signatures.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-112">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="6a3fd-113">Auparavant, UE-V incluait les modèles d’emplacement des paramètres Microsoft Office 2010 qui ont été automatiquement distribués et enregistrés auprès de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-113">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="6a3fd-114">UE-V 2,1 utilise Office 365 pour déterminer si les paramètres d’Office 2013 sont itinérants par Office 365.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-114">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="6a3fd-115">Si les paramètres sont itinérants par Office 365, ils ne sont pas itinérants par UE-V.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-115">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="6a3fd-116">La [vue d’ensemble des paramètres utilisateur et itinérance pour Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) fournit des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-116">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="6a3fd-117">Pour activer la synchronisation des paramètres avec UE-V 2,1, effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="6a3fd-117">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="6a3fd-118">Utiliser une stratégie de groupe pour désactiver la synchronisation d’Office 365</span><span class="sxs-lookup"><span data-stu-id="6a3fd-118">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="6a3fd-119">Ne pas activer l’interface de synchronisation Office 365 lors de l’installation d’Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a3fd-119">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="6a3fd-120">UE-V 2,1 inclut [les modèles office 2013 et office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="6a3fd-120">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="6a3fd-121">Cette version supprime les modèles Office 2007.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-121">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="6a3fd-122">Les utilisateurs peuvent toujours utiliser les modèles Office 2007 d’UE-V 2,0 ou une version antérieure et peuvent toujours obtenir les modèles de la Galerie de modèles UE-V située [ici](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="6a3fd-122">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>

## <span data-ttu-id="6a3fd-123">Résoudre les problèmes des utilisateurs d’espaces de noms du système de fichiers DFS</span><span class="sxs-lookup"><span data-stu-id="6a3fd-123">Fix for Distributed File System Namespace Users</span></span>


<span data-ttu-id="6a3fd-124">UE-V a amélioré la prise en charge du système de fichiers DFS en ajoutant une configuration UE-V appelée SyncProviderPingEnabled.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-124">UE-V has improved Distributed File System Namespace (DFSN) support by adding a UE-V configuration called SyncProviderPingEnabled.</span></span> <span data-ttu-id="6a3fd-125">La désactivation de cette configuration à l’aide de PowerShell ou WMI permet aux utilisateurs de désactiver le ping UE-V.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-125">Disabling this configuration using PowerShell or WMI allows users to disable the UE-V ping.</span></span> <span data-ttu-id="6a3fd-126">Dans le cas d’un serveur DFSN, le test ping d’UE-V génère une erreur, car ces serveurs ne répondent pas aux pings.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-126">The UE-V ping causes an error when using DFSN servers because these servers do not respond to pings.</span></span> <span data-ttu-id="6a3fd-127">Le non-réponse empêche UE-V de synchroniser les paramètres.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-127">The non-response prevents UE-V from synchronizing settings.</span></span> <span data-ttu-id="6a3fd-128">La désactivation de la commande ping UE-V autorise le fonctionnement normal de la synchronisation UE-V.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-128">Disabling the UE-V ping allows UE-V synchronization to work normally.</span></span>

<span data-ttu-id="6a3fd-129">Pour désactiver la commande ping UE-V, utilisez l’applet de commande PowerShell suivante:</span><span class="sxs-lookup"><span data-stu-id="6a3fd-129">To disable UE-V ping, use this PowerShell cmdlet:</span></span>

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## <span data-ttu-id="6a3fd-130">Synchronisation des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="6a3fd-130">Synchronization for Credentials</span></span>


<span data-ttu-id="6a3fd-131">UE-V 2,1 permet aux clients de synchroniser les informations d’identification et les certificats stockés dans le gestionnaire d’informations d’identification Windows.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-131">UE-V 2.1 gives customers the ability to synchronize credentials and certificates stored in the Windows Credential Manager.</span></span> <span data-ttu-id="6a3fd-132">Ce composant est désactivé par défaut.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-132">This component is disabled by default.</span></span> <span data-ttu-id="6a3fd-133">Lorsque ce composant est activé, les utilisateurs gardent leurs informations d’identification de domaine et leurs certificats synchronisés. Les utilisateurs peuvent se connecter une fois sur un appareil, et ces informations d’identification sont itinérantes pour cet utilisateur sur tous les appareils compatibles avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-133">Enabling this component lets users keep their domain credentials and certificates in sync. Users can sign in one time on a device, and these credentials will roam for that user across all of their UE-V enabled devices.</span></span> <span data-ttu-id="6a3fd-134">La [gestion des informations d’identification avec UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) fournit des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-134">[Manage Credentials with UE-V 2.1](https://technet.microsoft.com/library/dn458932.aspx#creds) provides more information.</span></span>

<span data-ttu-id="6a3fd-135">**Remarques**  Dans Windows 8 et versions ultérieures, le gestionnaire d’informations d’identification contient des informations d’identification Web.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-135">**Note** In Windows 8 and later, Credential Manager contains web credentials.</span></span> <span data-ttu-id="6a3fd-136">Ces informations d’identification ne sont pas synchronisées entre les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-136">These credentials are not synchronized between users’ devices.</span></span>

 

## <span data-ttu-id="6a3fd-137">UE-V et synchronisation de compte Microsoft</span><span class="sxs-lookup"><span data-stu-id="6a3fd-137">UE-V and Microsoft Account Synchronization</span></span>


<span data-ttu-id="6a3fd-138">UE-V détecte si les «paramètres de synchronisation avec OneDrive», également appelés «synchronisation de compte Microsoft», sont activés.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-138">UE-V detects if “Sync settings with OneDrive”, also known as Microsoft Account synchronization, is on.</span></span> <span data-ttu-id="6a3fd-139">Si le compte Microsoft n’est pas configuré pour synchroniser les paramètres, UE-V synchronise les applications Windows, les packages AppX et les paramètres de bureau Windows entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-139">If the Microsoft Account is not configured to synchronize settings, UE-V synchronizes Windows apps, AppX packages, and Windows desktop settings between devices.</span></span> <span data-ttu-id="6a3fd-140">Cela permet aux utilisateurs d’accéder à leurs applications du Windows Store, de la musique, des images et d’autres applications basées sur les comptes Microsoft sans être synchronisées en dehors du pare-feu de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-140">This lets users access their Store apps, music, pictures and other Microsoft Account-enabled applications without syncing outside of the enterprise firewall.</span></span> <span data-ttu-id="6a3fd-141">UE-V vérifie si la stratégie de groupe arrêtera de synchroniser les paramètres avec OneDrive ou si l’utilisateur désactive la **synchronisation de vos paramètres sur cet ordinateur** dans les contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-141">UE-V checks whether Group Policy will stop synchronizing settings with OneDrive or if the user disables **Sync your settings on this computer** in the user controls.</span></span>

## <span data-ttu-id="6a3fd-142">Support pour le PowerSchool externe</span><span class="sxs-lookup"><span data-stu-id="6a3fd-142">Support for the SyncMethod External</span></span>


<span data-ttu-id="6a3fd-143">Une nouvelle [configuration de PowerSchool](https://technet.microsoft.com/library/dn554321.aspx) appelée **externe** spécifie que si les paramètres d’UE-V sont écrits dans un dossier local sur l’ordinateur de l’utilisateur, tout moteur de synchronisation externe (par exemple, OneDrive entreprise, dossiers de travail, SharePoint ou Dropbox) peut être utilisé pour appliquer ces paramètres aux différents ordinateurs auxquels les utilisateurs accèdent.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-143">A new [SyncMethod configuration](https://technet.microsoft.com/library/dn554321.aspx) called **External** specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

## <span data-ttu-id="6a3fd-144">Prise en charge améliorée du mode VDI</span><span class="sxs-lookup"><span data-stu-id="6a3fd-144">Enhanced Support for VDI Mode</span></span>


<span data-ttu-id="6a3fd-145">UE-V 2,1 inclut la [prise en charge des sessions VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) partagées entre les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-145">UE-V 2.1 includes [support for VDI sessions](https://technet.microsoft.com/library/dn458932.aspx#vdi) that are shared among end users.</span></span> <span data-ttu-id="6a3fd-146">En tant qu’administrateur, vous pouvez enregistrer et configurer un modèle d’infrastructure VDI spéciale, qui permet de garantir le maintien de toutes ses fonctionnalités intactes pour les sessions VDI non persistantes.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-146">As an administrator, you can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

<span data-ttu-id="6a3fd-147">**Remarques**  Si vous n’activez pas le mode VDI pour les sessions VDI non persistantes, il est possible que certaines fonctionnalités ne fonctionnent pas, telles que sauvegarde et restauration et LKG.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-147">**Note** If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as back-up/restore and LKG.</span></span>

 

## <span data-ttu-id="6a3fd-148">Sauvegarde et restauration d’administration</span><span class="sxs-lookup"><span data-stu-id="6a3fd-148">Administrative Backup and Restore</span></span>


<span data-ttu-id="6a3fd-149">Vous pouvez restaurer des paramètres supplémentaires quand un utilisateur a adopté un nouvel appareil en plaçant un modèle d’emplacement des paramètres dans l’applet de connexion **Backup** ou **itinérance (par défaut)** à l’aide de l’applet de connexion Set-UevTemplateProfile PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-149">You can restore additional settings when a user adopts a new device by putting a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="6a3fd-150">Cela permet aux paramètres de l’ordinateur de se synchroniser avec le nouvel ordinateur, en plus des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-150">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="6a3fd-151">Les modèles attribués au profil de sauvegarde sont sauvegardés pour cet appareil et configurés sur une base par appareil.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-151">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="6a3fd-152">Pour plus d’informations, retrouvez la [sauvegarde et la restauration d’administration dans UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) .</span><span class="sxs-lookup"><span data-stu-id="6a3fd-152">[Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) provides more information.</span></span>

## <span data-ttu-id="6a3fd-153">Synchronisation pour les paramètres Windows supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6a3fd-153">Synchronization for Additional Windows Settings</span></span>


<span data-ttu-id="6a3fd-154">UE-V synchronise désormais la personnalisation du clavier visuel, le dictionnaire orthographique et permet le changement d’application pour les applications récentes et les paramètres de bord de l’écran à synchroniser entre les appareils Windows 8 et Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="6a3fd-154">UE-V now synchronizes touch keyboard personalization, the spelling dictionary, and enables the App Switching for recent apps and screen edge settings to synchronize between Windows 8 and Windows 8.1 devices.</span></span>






## <span data-ttu-id="6a3fd-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a3fd-155">Related topics</span></span>


[<span data-ttu-id="6a3fd-156">Prise en main d'UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="6a3fd-156">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="6a3fd-157">Préparer un déploiement UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="6a3fd-157">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="6a3fd-158">Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1</span><span class="sxs-lookup"><span data-stu-id="6a3fd-158">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





