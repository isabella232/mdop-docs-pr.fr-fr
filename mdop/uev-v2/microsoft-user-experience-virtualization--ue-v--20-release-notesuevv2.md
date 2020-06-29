---
title: Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0
description: Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811063"
---
# <span data-ttu-id="14701-103">Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.0</span><span class="sxs-lookup"><span data-stu-id="14701-103">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>


<span data-ttu-id="14701-104">Pour effectuer une recherche dans les notes de publication de Microsoft User Interface (UE-V) 2,0, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="14701-104">To search Microsoft User Experience Virtualization (UE-V) 2.0 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="14701-105">Nous vous conseillons de lire soigneusement ces notes de publication avant d’installer UE-V.</span><span class="sxs-lookup"><span data-stu-id="14701-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="14701-106">Les notes de publication contiennent des informations nécessaires à l’installation réussie de la virtualisation de l’interface utilisateur et contiennent des informations supplémentaires qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="14701-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="14701-107">S’il existe des différences entre ces notes de publication et d’autres documents UE-V, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="14701-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="14701-108">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="14701-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="14701-109">Envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="14701-109">Providing feedback</span></span>


<span data-ttu-id="14701-110">Dites-nous ce que vous pensez de notre documentation pour MDOP en nous fournissant vos commentaires et commentaires.</span><span class="sxs-lookup"><span data-stu-id="14701-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="14701-111">Envoyez votre commentaires de documentation à [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="14701-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="14701-112">UE-V problèmes connus</span><span class="sxs-lookup"><span data-stu-id="14701-112">UE-V known issues</span></span>


<span data-ttu-id="14701-113">Cette section contient des notes de publication relatives à la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14701-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="14701-114">Les paramètres de registre ne sont pas synchronisés entre App-V et les applications natives sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="14701-114">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="14701-115">Lorsqu’un ordinateur dispose d’une application installée par le biais de la virtualisation des applications (App-V) et d’une application locale avec un fichier Windows Installer (. msi), les paramètres basés sur le registre ne sont pas synchronisés entre les technologies.</span><span class="sxs-lookup"><span data-stu-id="14701-115">When a computer has an application that is installed through both Application Virtualization (App-V) and a locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="14701-116">**Solution de contournement:** Pour résoudre ce problème, exécutez l’application en sélectionnant l’une des deux technologies, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="14701-116">**WORKAROUND:** To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="14701-117">Les paramètres ne sont pas synchronisés lorsque le partage réseau se trouve hors du domaine de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="14701-117">Settings do not synchronization when network share is outside user’s domain</span></span>

<span data-ttu-id="14701-118">Lorsque Windows® 8 tente de synchroniser les paramètres du système d’exploitation, la synchronisation échoue avec le message d’erreur suivant: **Boost:: FileSystem:: existe:: nom d’utilisateur ou mot de passe incorrect**.</span><span class="sxs-lookup"><span data-stu-id="14701-118">When Windows® 8 attempts operating system settings synchronization, the synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="14701-119">Cette erreur peut indiquer que le partage réseau se trouve en dehors du domaine de l’utilisateur ou d’un domaine ayant une relation d’approbation avec ce domaine.</span><span class="sxs-lookup"><span data-stu-id="14701-119">This error can indicate that the network share is outside the user’s domain or a domain with a trust relationship to that domain.</span></span> <span data-ttu-id="14701-120">Pour vérifier les événements du journal opérationnel, ouvrez l' **Observateur d’événements** et naviguez jusqu’à **applications et services consigne**le fonctionnement de l’enregistrement de la virtualisation de l'  /  **Microsoft**  /  **interface utilisateur**de Microsoft  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="14701-120">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="14701-121">Les partages réseau utilisés pour les emplacements de stockage des paramètres UE-V doivent résider dans le même domaine Active Directory que l’utilisateur ou un domaine approuvé du domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14701-121">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user or a trusted domain of the user’s domain.</span></span>

<span data-ttu-id="14701-122">**Solution de contournement:** Utilisez les partages réseau du même domaine Active Directory que l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14701-122">**WORKAROUND:** Use network shares from the same Active Directory domain as the user.</span></span>

### <span data-ttu-id="14701-123">Résultats inattendus avec Office 2010 et Office 2013 installés</span><span class="sxs-lookup"><span data-stu-id="14701-123">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="14701-124">Lorsqu’un utilisateur a installé Office 2010 et Office 2013, tous les paramètres courants entre les deux versions d’Office sont itinérants par UE-V.</span><span class="sxs-lookup"><span data-stu-id="14701-124">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="14701-125">Cela risque de rendre la taille du package Office 2010 trop importante ou engendrer des conflits inattendus avec 2013, en particulier si la version d’Office 365 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="14701-125">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="14701-126">**Solution de contournement:** Installer une seule version d’Office ou limiter les paramètres qui sont synchronisés par UE-V.</span><span class="sxs-lookup"><span data-stu-id="14701-126">**WORKAROUND:** Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="14701-127">La désinstallation de l’application Windows 8 rétablit les paramètres à l’état initial</span><span class="sxs-lookup"><span data-stu-id="14701-127">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="14701-128">Lors de l’utilisation de la synchronisation des paramètres d’UE-V pour une application Windows 8, si l’utilisateur désinstalle l’application, puis réinstalle l’application, les paramètres de l’application rétablissent leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="14701-128">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="14701-129">Ce problème se produit car la désinstallation supprime la copie locale (mise en cache) des paramètres de l’application, mais ne supprime pas le package de paramètres UE-V local.</span><span class="sxs-lookup"><span data-stu-id="14701-129"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="14701-130">Lorsque l’application est réinstallée et lancée, UE-V rassemblez les paramètres d’application qui ont été réinitialisés aux valeurs par défaut de l’application, puis chargez les paramètres par défaut sur l’emplacement de stockage central.</span><span class="sxs-lookup"><span data-stu-id="14701-130"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="14701-131">D’autres ordinateurs exécutant l’application téléchargent les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="14701-131"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="14701-132">Ce comportement est identique au comportement des applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="14701-132"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="14701-133">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="14701-133">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="14701-134">Signature électronique de signature pour Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="14701-134">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="14701-135">UE-V va itinérance des fichiers de signature Outlook 2010 entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="14701-135">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="14701-136">Toutefois, les options de signature par défaut pour les nouveaux messages, les réponses aux messages et les transferts ne sont pas synchronisées.</span><span class="sxs-lookup"><span data-stu-id="14701-136">However, the default signature options for new messages and replies or forwards are not synchronized.</span></span> <span data-ttu-id="14701-137">Ces deux paramètres sont stockés dans le profil Outlook, dont UE-V n’est pas itinérant.</span><span class="sxs-lookup"><span data-stu-id="14701-137">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="14701-138">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="14701-138">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="14701-139">UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="14701-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="14701-140">Nous vous recommandons d’installer la version 64 de Microsoft Office pour les ordinateurs modernes.</span><span class="sxs-lookup"><span data-stu-id="14701-140">We recommend that you install the 64-bit version of Microsoft Office for modern computers.</span></span> <span data-ttu-id="14701-141">Pour déterminer la version dont vous avez besoin, [cliquez ici](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span><span class="sxs-lookup"><span data-stu-id="14701-141">To determine which version you need, [click here](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span></span> <span data-ttu-id="14701-142">UE-V prend en charge les paramètres d’itinérance entre les différentes versions de l’architecture d’Office.</span><span class="sxs-lookup"><span data-stu-id="14701-142">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="14701-143">Par exemple, les paramètres d’Office 32 bits s’itinérance entre toutes les instances Office 32 bits.</span><span class="sxs-lookup"><span data-stu-id="14701-143">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="14701-144">UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="14701-144">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="14701-145">**Solution de contournement:** Néant</span><span class="sxs-lookup"><span data-stu-id="14701-145">**WORKAROUND:** None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="14701-146">Les MSI ne sont pas localisés</span><span class="sxs-lookup"><span data-stu-id="14701-146">MSI’s are not localized</span></span>

<span data-ttu-id="14701-147">UE-V 2,0 inclut un programme d’installation localisé pour l’agent UE-V et le générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="14701-147">UE-V 2.0 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="14701-148">Ils sont toujours disponibles, mais l’interface utilisateur est réduite et l’affichage du MSI uniquement en anglais.</span><span class="sxs-lookup"><span data-stu-id="14701-148">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="14701-149">Malgré le fichier en anglais, le programme d’installation installe toutes les langues prises en charge lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="14701-149">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="14701-150">**Solution de contournement:** Néant</span><span class="sxs-lookup"><span data-stu-id="14701-150">**WORKAROUND:** None</span></span>

### <span data-ttu-id="14701-151">Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants</span><span class="sxs-lookup"><span data-stu-id="14701-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="14701-152">Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants par la virtualisation de l’interface utilisateur et qui n’apparaissent pas à la première apparition des favoris sur un nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="14701-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="14701-153">**Solution de contournement:** Favicons s’affiche avec les favoris associés lorsque le signet est utilisé et mis en cache dans le navigateur Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="14701-153">**WORKAROUND:** Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="14701-154">Les chemins d’accès aux paramètres de fichier sont stockés dans le registre</span><span class="sxs-lookup"><span data-stu-id="14701-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="14701-155">Certains paramètres d’application stockent les chemins d’accès de leurs fichiers de configuration et de paramètres en tant que valeurs dans le registre.</span><span class="sxs-lookup"><span data-stu-id="14701-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="14701-156">Les fichiers référencés sous forme de chemin d’accès dans le registre doivent être synchronisés lorsque les paramètres sont itinérants entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="14701-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="14701-157">**Solution de contournement:** Utilisez la redirection de dossiers ou d’autres technologies pour vous assurer que tous les fichiers référencés comme chemins d’accès aux paramètres de fichier sont présents et placés au même emplacement sur tous les ordinateurs dans lesquels les paramètres sont itinérants.</span><span class="sxs-lookup"><span data-stu-id="14701-157">**WORKAROUND:** Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="14701-158">Les chemins de stockage de paramètres longs peuvent générer une erreur</span><span class="sxs-lookup"><span data-stu-id="14701-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="14701-159">Le raccourci de stockage des paramètres reste le plus court possible.</span><span class="sxs-lookup"><span data-stu-id="14701-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="14701-160">Les chemins longs peuvent empêcher la résolution ou la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="14701-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="14701-161">UE-V utilise le chemin de stockage des paramètres dans le cadre du chemin d’accès calculé au stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="14701-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="14701-162">Ce chemin d’accès est calculé comme suit: Path Storage path + "settingspackages" + package dir (ID de modèle) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="14701-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="14701-163">Si le chemin d’accès calculé est supérieur à 260 caractères, le stockage du package échoue et génère le message d’erreur suivant dans le journal des événements de fonctionnement d’UE-V:</span><span class="sxs-lookup"><span data-stu-id="14701-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="14701-164">Pour vérifier les événements du journal opérationnel, ouvrez l’observateur d’événements et naviguez jusqu’à la section journaux des applications et des services/Microsoft/User-Virtualization/Logging/Operations.</span><span class="sxs-lookup"><span data-stu-id="14701-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="14701-165">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="14701-165">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="14701-166">Certains paramètres du système d’exploitation ne suivent que les versions du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="14701-166">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="14701-167">Les paramètres du système d’exploitation pour le narrateur et les caractères de devise spécifiques aux paramètres régionaux (par exemple, les paramètres linguistiques et régionaux) ne sont itinérants que sur les versions de système d’exploitation de Windows.</span><span class="sxs-lookup"><span data-stu-id="14701-167">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="14701-168">Par exemple, les caractères monétaires ne seront pas itinérants entre Windows 7 et Windows 8.</span><span class="sxs-lookup"><span data-stu-id="14701-168">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="14701-169">**Solution de contournement:** Néant</span><span class="sxs-lookup"><span data-stu-id="14701-169">**WORKAROUND:** None</span></span>

### <span data-ttu-id="14701-170">Les applications Windows 8 ne synchronisent pas les paramètres lors du redémarrage de l’application</span><span class="sxs-lookup"><span data-stu-id="14701-170">Windows 8 apps do not sync settings when the app restarts after closing unexpectedly</span></span>

<span data-ttu-id="14701-171">Si une application Windows 8 se ferme de manière inattendue après le démarrage, les paramètres de l’application risquent de ne pas être synchronisés lors du redémarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="14701-171">If a Windows 8 app closes unexpectedly soon after startup, settings for the application may not be synchronized when the application is restarted.</span></span>

<span data-ttu-id="14701-172">**Solution de contournement:** Fermez l’application Windows 8, fermez et redémarrez l’application UevAppMonitor.exe (peut utiliser TaskManager), puis redémarrez l’application Windows 8.</span><span class="sxs-lookup"><span data-stu-id="14701-172">**WORKAROUND:** Close the Windows 8 app, close and restart the UevAppMonitor.exe application (can use TaskManager), and then restart the Windows 8 app.</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="14701-173">UE-V 1 agent génère des erreurs lors de l’exécution de modèles UE-V 2</span><span class="sxs-lookup"><span data-stu-id="14701-173">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="14701-174">Si un modèle d’emplacement des paramètres d’UE-V 2 est distribué sur un ordinateur installé avec un agent UE-V 1, certains paramètres ne sont pas synchronisés entre les ordinateurs et l’agent signale les erreurs dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="14701-174">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="14701-175">**Solution de contournement:** Lors de la migration de UE-V 1 vers UE-V 2, il est possible que vous disposiez d’ordinateurs exécutant la version précédente de l’agent, que vous ayez créé un catalogue UE-V 2,0 distinct pour la prise en charge des modèles et de l’agent 2,0.</span><span class="sxs-lookup"><span data-stu-id="14701-175">**WORKAROUND:** When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.0 catalog to support the UE-V 2.0 Agent and templates.</span></span>

## <span data-ttu-id="14701-176">HotFix et Articles de la base de connaissances pour UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="14701-176">Hotfixes and Knowledge Base articles for UE-V 2.0</span></span>


<span data-ttu-id="14701-177">Cette section contient des correctifs et des Articles de la base de connaissances pour UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="14701-177">This section contains hotfixes and KB articles for UE-V 2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="14701-178">Article de la base de connaissances</span><span class="sxs-lookup"><span data-stu-id="14701-178">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="14701-179">Title</span><span class="sxs-lookup"><span data-stu-id="14701-179">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="14701-180">Link</span><span class="sxs-lookup"><span data-stu-id="14701-180">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14701-181">2927019</span><span class="sxs-lookup"><span data-stu-id="14701-181">2927019</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-182">Package Hotfix 1 pour les utilisateurs de Microsoft-virtualisation 2,0</span><span class="sxs-lookup"><span data-stu-id="14701-182">Hotfix Package 1 for Microsoft User Experience Virtualization 2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)"><span data-ttu-id="14701-183">support.microsoft.com/kb/2927019</span><span class="sxs-lookup"><span data-stu-id="14701-183">support.microsoft.com/kb/2927019</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14701-184">2903501</span><span class="sxs-lookup"><span data-stu-id="14701-184">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-185">UE-V: compatibilité entre les utilisateurs et la virtualisation de l’interface utilisateur avec les profils utilisateur</span><span class="sxs-lookup"><span data-stu-id="14701-185">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="14701-186">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-186">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14701-187">2770042</span><span class="sxs-lookup"><span data-stu-id="14701-187">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-188">Paramètres de Registre UE-V</span><span class="sxs-lookup"><span data-stu-id="14701-188">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="14701-189">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-189">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14701-190">2847017</span><span class="sxs-lookup"><span data-stu-id="14701-190">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-191">Paramètres d’UE-V répliqués par Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="14701-191">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="14701-192">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-192">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14701-193">2930271</span><span class="sxs-lookup"><span data-stu-id="14701-193">2930271</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-194">Présentation des limitations des signatures Outlook en itinérance dans Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="14701-194">Understanding the limitations of roaming Outlook signatures in Microsoft UE-V</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)"><span data-ttu-id="14701-195">support.microsoft.com/kb/2930271/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-195">support.microsoft.com/kb/2930271/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14701-196">2769631</span><span class="sxs-lookup"><span data-stu-id="14701-196">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-197">Réparation d’une installation d’UE-V endommagée</span><span class="sxs-lookup"><span data-stu-id="14701-197">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="14701-198">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-198">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14701-199">2850989</span><span class="sxs-lookup"><span data-stu-id="14701-199">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-200">La migration de profils MAPI avec Microsoft UE-V n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="14701-200">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="14701-201">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-201">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14701-202">2769586</span><span class="sxs-lookup"><span data-stu-id="14701-202">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-203">UE-V: itinérance de dossiers et de clés de Registre vides</span><span class="sxs-lookup"><span data-stu-id="14701-203">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="14701-204">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-204">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14701-205">2782997</span><span class="sxs-lookup"><span data-stu-id="14701-205">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-206">Comment activer la journalisation de débogage dans Microsoft User Interface Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="14701-206">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="14701-207">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-207">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14701-208">2769570</span><span class="sxs-lookup"><span data-stu-id="14701-208">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-209">UE-V ne met pas à jour le thème pour les sessions RDS ou VDI</span><span class="sxs-lookup"><span data-stu-id="14701-209">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="14701-210">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-210">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14701-211">2901856</span><span class="sxs-lookup"><span data-stu-id="14701-211">2901856</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-212">Les paramètres de l’application ne se synchronisent pas après le redémarrage sur un ordinateur avec UE-V</span><span class="sxs-lookup"><span data-stu-id="14701-212">Application settings do not sync after you force a restart on a UE-V-enabled computer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)"><span data-ttu-id="14701-213">support.microsoft.com/kb/2901856/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-213">support.microsoft.com/kb/2901856/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14701-214">2850582</span><span class="sxs-lookup"><span data-stu-id="14701-214">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-215">Utiliser la virtualisation de l’utilisation de Microsoft avec les applications App-V</span><span class="sxs-lookup"><span data-stu-id="14701-215">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="14701-216">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-216">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14701-217">3041879</span><span class="sxs-lookup"><span data-stu-id="14701-217">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-218">Versions de fichiers actuelles pour l’utilisation de Microsoft User-virtualisation</span><span class="sxs-lookup"><span data-stu-id="14701-218">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="14701-219">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-219">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14701-220">2843592</span><span class="sxs-lookup"><span data-stu-id="14701-220">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="14701-221">Informations sur la virtualisation et la disponibilité des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="14701-221">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="14701-222">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="14701-222">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





