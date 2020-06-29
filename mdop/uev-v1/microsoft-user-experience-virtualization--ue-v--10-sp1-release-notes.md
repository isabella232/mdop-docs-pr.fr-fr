---
title: Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0SP1
description: Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0SP1
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804261"
---
# <span data-ttu-id="6af8a-103">Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0SP1</span><span class="sxs-lookup"><span data-stu-id="6af8a-103">Microsoft User Experience Virtualization (UE-V) 1.0 SP1 Release Notes</span></span>


<span data-ttu-id="6af8a-104">Pour effectuer une recherche dans les notes de publication de Microsoft User Interface (UE-V) 1,0 Service Pack 1, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="6af8a-104">To search Microsoft User Experience Virtualization (UE-V) 1.0 Service Pack 1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="6af8a-105">Nous vous conseillons de lire soigneusement ces notes de publication avant d’installer UE-V.</span><span class="sxs-lookup"><span data-stu-id="6af8a-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="6af8a-106">Les notes de publication contiennent des informations nécessaires à l’installation réussie de la virtualisation de l’interface utilisateur et contiennent des informations supplémentaires qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="6af8a-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="6af8a-107">S’il existe des différences entre ces notes de publication et d’autres documents UE-V, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="6af8a-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="6af8a-108">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="6af8a-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="6af8a-109">UE-V problèmes connus</span><span class="sxs-lookup"><span data-stu-id="6af8a-109">UE-V known issues</span></span>


<span data-ttu-id="6af8a-110">Cette section contient des notes de publication relatives à l’utilisation de User Virtualization 1,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="6af8a-110">This section contains release notes for User Experience Virtualization 1.0 SP1.</span></span>

### <span data-ttu-id="6af8a-111">Les paramètres de registre ne peuvent pas être synchronisés entre les applications App-V et natives sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="6af8a-111">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="6af8a-112">Lorsqu’un ordinateur dispose d’une application disponible via l’application Application Virtualization (App-V) et une application d’installation Native installée avec un programme d’installation Windows (fichier. msi), les paramètres basés sur le registre ne sont pas synchronisés entre les technologies.</span><span class="sxs-lookup"><span data-stu-id="6af8a-112">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application installed with a Windows Installer (.msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="6af8a-113">SOLUTION: pour résoudre ce problème, exécutez l’application en sélectionnant l’une des deux technologies, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="6af8a-113">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="6af8a-114">La synchronisation de paramètres de Windows 8 échoue lorsque le partage réseau se trouve hors du domaine de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="6af8a-114">Windows 8 setting synchronization fails when network share is outside user’s domain</span></span>

<span data-ttu-id="6af8a-115">Lorsque Windows® 8 tente d’utiliser la synchronisation des paramètres du système d’exploitation, l’synchrnization échoue avec le message d’erreur suivant: **Boost:: FileSystem:: exists: nom d’utilisateur ou mot de passe incorrect**.</span><span class="sxs-lookup"><span data-stu-id="6af8a-115">When Windows® 8 attempts operating system settings synchronization, the synchrnization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="6af8a-116">Cette erreur peut indiquer que le partage réseau se trouve en dehors du domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6af8a-116">This error can indicate that the network share is outside the user’s domain.</span></span> <span data-ttu-id="6af8a-117">Pour vérifier les événements du journal opérationnel, ouvrez l' **Observateur d’événements** et naviguez jusqu’à **applications et services consigne**le fonctionnement de l’enregistrement de la virtualisation de l'  /  **Microsoft**  /  **interface utilisateur**de Microsoft  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="6af8a-117">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="6af8a-118">Les partages réseau utilisés pour les emplacements de stockage des paramètres UE-V doivent résider dans le même domaine Active Directory que l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6af8a-118">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span>

<span data-ttu-id="6af8a-119">SOLUTION: utilisez les partages réseau du même domaine Active Directory que l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6af8a-119">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="6af8a-120">.</span><span class="sxs-lookup"><span data-stu-id="6af8a-120">.</span></span>

### <span data-ttu-id="6af8a-121">Signature électronique de signature pour Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="6af8a-121">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="6af8a-122">UE-V va itinérance des fichiers de signature Outlook 2010 entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="6af8a-122">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="6af8a-123">Toutefois, les options de signature par défaut pour les nouveaux messages et les réponses/transferts ne sont pas itinérantes.</span><span class="sxs-lookup"><span data-stu-id="6af8a-123">However, the default signature options for new messages and replies/forwards are not roamed.</span></span> <span data-ttu-id="6af8a-124">Ces deux paramètres sont stockés dans le profil Outlook, dont UE-V n’est pas itinérant.</span><span class="sxs-lookup"><span data-stu-id="6af8a-124">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="6af8a-125">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="6af8a-125">WORKAROUND: None.</span></span>

### <span data-ttu-id="6af8a-126">Les paramètres de synchronisation ne sont pas synchronisés à l’intervalle attendu lors de l’exécution en mode de liaison lente</span><span class="sxs-lookup"><span data-stu-id="6af8a-126">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="6af8a-127">Dans des conditions normales, les emplacements de stockage des paramètres doivent être disponibles sur une connexion réseau rapide.</span><span class="sxs-lookup"><span data-stu-id="6af8a-127">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="6af8a-128">Le mode de liaison lente est uniquement exécuté de manière périodique.</span><span class="sxs-lookup"><span data-stu-id="6af8a-128">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="6af8a-129">Par défaut, la planification de la synchronisation du mode de liaison lente est définie sur toutes les 360 minutes.</span><span class="sxs-lookup"><span data-stu-id="6af8a-129">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="6af8a-130">Solution de contournement: pour modifier la fréquence de synchronisation en arrière-plan des ordinateurs en mode de liaison lente, vous pouvez configurer la stratégie de groupe pour la stratégie de synchronisation en arrière-plan pour les **fichiers en mode hors connexion**.</span><span class="sxs-lookup"><span data-stu-id="6af8a-130">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="6af8a-131">Les caractères spéciaux ne sont pas synchronisés</span><span class="sxs-lookup"><span data-stu-id="6af8a-131">Special characters do not synchronize</span></span>

<span data-ttu-id="6af8a-132">Certains caractères, tels que les symboles monétaires, ne sont pas synchronisés entre les ordinateurs Windows 7 et Windows 8 qui exécutent l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="6af8a-132">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="6af8a-133">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="6af8a-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="6af8a-134">UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="6af8a-134">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="6af8a-135">Nous vous recommandons d’installer la version 32 bits de Microsoft Office pour les systèmes d’exploitation 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6af8a-135">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="6af8a-136">Pour choisir la version de Microsoft Office dont vous avez besoin, cliquez ici ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ).</span><span class="sxs-lookup"><span data-stu-id="6af8a-136">To choose the Microsoft Office version that you need, click here ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="6af8a-137">UE-V prend en charge les paramètres d’itinérance entre les différentes versions de l’architecture d’Office.</span><span class="sxs-lookup"><span data-stu-id="6af8a-137">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="6af8a-138">Par exemple, les paramètres d’Office 32 bits s’itinérance entre toutes les instances Office 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6af8a-138">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="6af8a-139">UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="6af8a-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="6af8a-140">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="6af8a-140">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="6af8a-141">Les MSI ne sont pas localisés</span><span class="sxs-lookup"><span data-stu-id="6af8a-141">MSI’s are not localized</span></span>

<span data-ttu-id="6af8a-142">UE-V 1,0 SP1 inclut un programme d’installation localisé pour les agents UE-V et UE-V.</span><span class="sxs-lookup"><span data-stu-id="6af8a-142">UE-V 1.0 SP1 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="6af8a-143">Ils sont toujours disponibles, mais l’interface utilisateur est réduite et l’affichage du MSI uniquement en anglais.</span><span class="sxs-lookup"><span data-stu-id="6af8a-143">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="6af8a-144">Malgré le fichier en anglais, le programme d’installation installe toutes les langues prises en charge lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="6af8a-144">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="6af8a-145">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="6af8a-145">WORKAROUND: None</span></span>

### <span data-ttu-id="6af8a-146">Les autres dossiers du partage avec l’emplacement de stockage des paramètres ne sont pas disponibles en mode de connexion lente.</span><span class="sxs-lookup"><span data-stu-id="6af8a-146">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="6af8a-147">Les partages du magasin de valeurs doivent se trouver sur un partage réseau qui est utilisé pour les autres dossiers qui doivent toujours être disponibles.</span><span class="sxs-lookup"><span data-stu-id="6af8a-147">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="6af8a-148">Lorsque le partage réseau qui héberge l’emplacement de stockage des paramètres passe en mode de connexion lente, le seul dossier disponible est le dossier d’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="6af8a-148">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="6af8a-149">Les autres dossiers du partage ne sont pas disponibles en mode de connexion lente.</span><span class="sxs-lookup"><span data-stu-id="6af8a-149">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="6af8a-150">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="6af8a-150">Workaround: None</span></span>

### <span data-ttu-id="6af8a-151">Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants</span><span class="sxs-lookup"><span data-stu-id="6af8a-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="6af8a-152">Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants par la virtualisation de l’interface utilisateur et qui n’apparaissent pas à la première apparition des favoris sur un nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6af8a-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="6af8a-153">SOLUTION: favicons apparaît avec les favoris associés une fois que le signet est utilisé et mis en cache dans le navigateur Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6af8a-153">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="6af8a-154">Les chemins d’accès aux paramètres de fichier sont stockés dans le registre</span><span class="sxs-lookup"><span data-stu-id="6af8a-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="6af8a-155">Certains paramètres d’application stockent les chemins d’accès de leurs fichiers de configuration et de paramètres en tant que valeurs dans le registre.</span><span class="sxs-lookup"><span data-stu-id="6af8a-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="6af8a-156">Les fichiers référencés sous forme de chemin d’accès dans le registre doivent être synchronisés lorsque les paramètres sont itinérants entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6af8a-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="6af8a-157">Solution de contournement: utilisez la redirection de dossiers ou d’autres technologies pour vous assurer que tous les fichiers référencés comme chemins d’accès aux paramètres de fichier sont présents et placés au même emplacement sur tous les ordinateurs dans lesquels les paramètres sont itinérants.</span><span class="sxs-lookup"><span data-stu-id="6af8a-157">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="6af8a-158">Les chemins de stockage de paramètres longs peuvent générer une erreur</span><span class="sxs-lookup"><span data-stu-id="6af8a-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="6af8a-159">Le raccourci de stockage des paramètres reste le plus court possible.</span><span class="sxs-lookup"><span data-stu-id="6af8a-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="6af8a-160">Les chemins longs peuvent empêcher la résolution ou la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6af8a-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="6af8a-161">UE-V utilise le chemin de stockage des paramètres dans le cadre du chemin d’accès calculé au stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="6af8a-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="6af8a-162">Ce chemin d’accès est calculé comme suit: Path Storage path + "settingspackages" + package dir (ID de modèle) + nom du package (ID de modèle).</span><span class="sxs-lookup"><span data-stu-id="6af8a-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID).</span></span> <span data-ttu-id="6af8a-163">Si le chemin d’accès calculé est supérieur à 260 caractères, le stockage du package échoue et génère le message d’erreur suivant dans le journal des événements de fonctionnement d’UE-V:</span><span class="sxs-lookup"><span data-stu-id="6af8a-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="6af8a-164">Pour vérifier les événements du journal opérationnel, ouvrez l’observateur d’événements et naviguez jusqu’à la section journaux des applications et des services/Microsoft/User-Virtualization/Logging/Operations.</span><span class="sxs-lookup"><span data-stu-id="6af8a-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="6af8a-165">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="6af8a-165">WORKAROUND: None.</span></span>

### <span data-ttu-id="6af8a-166">UE-V agent retarde lors de la connexion ou de la connexion</span><span class="sxs-lookup"><span data-stu-id="6af8a-166">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="6af8a-167">Si une connexion ou une connexion se produit avant que les fichiers hors connexion n’aient déterminé qu’une liaison lente est en place, la déconnexion ou la connexion peuvent être retardées.</span><span class="sxs-lookup"><span data-stu-id="6af8a-167">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="6af8a-168">La fonctionnalité fichiers en mode hors connexion ne doit pas durer jusqu’à trois minutes pour détecter l’état actuel du réseau.</span><span class="sxs-lookup"><span data-stu-id="6af8a-168">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="6af8a-169">Si la connexion ou l’arrêt se produit avant que les fichiers hors connexion n’aient déterminé que l’ordinateur est connecté à une liaison lente, le package de paramètres d’UE-V sera envoyé au serveur au lieu du cache local.</span><span class="sxs-lookup"><span data-stu-id="6af8a-169">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="6af8a-170">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="6af8a-170">WORKAROUND: None.</span></span>

### <span data-ttu-id="6af8a-171">Conflit de paramètres lors de la tentative d’itinérance des paramètres du système d’exploitation sur Windows 8</span><span class="sxs-lookup"><span data-stu-id="6af8a-171">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="6af8a-172">Dans Windows 8, si la synchronisation de compte Microsoft est activée avec UE-V pour les paramètres du système d’exploitation, les paramètres appliqués peuvent être incohérents.</span><span class="sxs-lookup"><span data-stu-id="6af8a-172">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="6af8a-173">Solution de contournement: effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="6af8a-173">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="6af8a-174">Désactiver la synchronisation des comptes Microsoft si vous utilisez UE-V pour itinérance dans les paramètres du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6af8a-174">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="6af8a-175">Désactiver UE-V pour les paramètres du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6af8a-175">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="6af8a-176">Certains paramètres du système d’exploitation ne suivent que les versions du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6af8a-176">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="6af8a-177">Les paramètres du système d’exploitation pour le narrateur et les caractères de devise spécifiques aux paramètres régionaux ne seront itinérants que sur les versions de système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="6af8a-177">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="6af8a-178">Par exemple, les caractères monétaires ne seront déplacés que de Windows 7 vers Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6af8a-178">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="6af8a-179">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="6af8a-179">WORKAROUND: None</span></span>

 

 





