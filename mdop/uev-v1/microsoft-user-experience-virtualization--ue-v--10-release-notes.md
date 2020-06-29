---
title: Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0
description: Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804266"
---
# <span data-ttu-id="6a607-103">Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0</span><span class="sxs-lookup"><span data-stu-id="6a607-103">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>


<span data-ttu-id="6a607-104">Pour effectuer une recherche dans les notes de publication de Microsoft User Interface (UE-V), appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="6a607-104">To search Microsoft User Experience Virtualization (UE-V) release notes, press Ctrl+F.</span></span>

<span data-ttu-id="6a607-105">Nous vous conseillons de lire soigneusement ces notes de publication avant d’installer UE-V.</span><span class="sxs-lookup"><span data-stu-id="6a607-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="6a607-106">Les notes de publication contiennent des informations nécessaires à l’installation réussie de la virtualisation de l’interface utilisateur et contiennent des informations supplémentaires qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="6a607-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="6a607-107">S’il existe des différences entre ces notes de publication et d’autres documents UE-V, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="6a607-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="6a607-108">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="6a607-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="6a607-109">Envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="6a607-109">Providing feedback</span></span>


<span data-ttu-id="6a607-110">Dites-nous ce que vous pensez de notre documentation pour MDOP en nous fournissant vos commentaires et commentaires.</span><span class="sxs-lookup"><span data-stu-id="6a607-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="6a607-111">Envoyez votre commentaires de documentation à [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="6a607-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="6a607-112">UE-V problèmes connus</span><span class="sxs-lookup"><span data-stu-id="6a607-112">UE-V known issues</span></span>


<span data-ttu-id="6a607-113">Cette section contient des notes de publication relatives à la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a607-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="6a607-114">Les paramètres de registre ne peuvent pas être synchronisés entre les applications App-V et natives sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="6a607-114">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="6a607-115">Lorsqu’un ordinateur dispose d’une application disponible via l’application Application Virtualization (App-V) et une application d’installation native (installée avec un fichier. msi), les paramètres basés sur le registre ne sont pas synchronisés entre les technologies.</span><span class="sxs-lookup"><span data-stu-id="6a607-115">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application (installed with an .msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="6a607-116">SOLUTION: pour résoudre ce problème, exécutez l’application en sélectionnant l’une des deux technologies, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="6a607-116">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="6a607-117">La synchronisation des paramètres de Windows 8 échoue avec un message d’erreur: «Booster:: FileSystem:: existe:: nom d’utilisateur ou mot de passe incorrect»</span><span class="sxs-lookup"><span data-stu-id="6a607-117">Windows 8 setting synchronization fails with error: "boost::filesystem::exists::Incorrect user name or password"</span></span>

<span data-ttu-id="6a607-118">La synchronisation des paramètres du système d’exploitation Windows® 8 échoue avec le message d’erreur suivant: **Boost:: FileSystem:: existe:: nom d’utilisateur ou mot de passe incorrect**.</span><span class="sxs-lookup"><span data-stu-id="6a607-118">The Windows® 8 operating system settings synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="6a607-119">Pour vérifier les événements du journal opérationnel, ouvrez l' **Observateur d’événements** et naviguez jusqu’à **applications et services consigne**le fonctionnement de l’enregistrement de la virtualisation de l'  /  **Microsoft**  /  **interface utilisateur**de Microsoft  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="6a607-119">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="6a607-120">Les partages réseau utilisés pour les emplacements de stockage des paramètres UE-V doivent résider dans le même domaine Active Directory que l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a607-120">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span> <span data-ttu-id="6a607-121">Dans le cas contraire, l’erreur suivante peut s’afficher: «nom d’utilisateur ou mot de passe incorrect».</span><span class="sxs-lookup"><span data-stu-id="6a607-121">Otherwise, the following error might occur: "Incorrect user name or password".</span></span>

<span data-ttu-id="6a607-122">SOLUTION: utilisez les partages réseau du même domaine Active Directory que l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a607-122">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="6a607-123">.</span><span class="sxs-lookup"><span data-stu-id="6a607-123">.</span></span>

### <span data-ttu-id="6a607-124">Signature électronique de signature pour Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="6a607-124">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="6a607-125">UE-V va itinérance des fichiers de signature Outlook 2010 entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="6a607-125">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="6a607-126">Toutefois, les options de signature par défaut pour les nouveaux messages et les réponses/transferts ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="6a607-126">However, the default signature options for new messages and replies/forwards are not.</span></span><span data-ttu-id="6a607-127">Ces deux paramètres sont stockés dans le profil Outlook, que UE-Vdoes n’est pas itinérant.</span><span class="sxs-lookup"><span data-stu-id="6a607-127"> These two settings are stored in the Outlook profile, which UE-Vdoes not roam.</span></span>

<span data-ttu-id="6a607-128">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="6a607-128">WORKAROUND: None.</span></span>

### <span data-ttu-id="6a607-129">Les paramètres de synchronisation ne sont pas synchronisés à l’intervalle attendu lors de l’exécution en mode de liaison lente</span><span class="sxs-lookup"><span data-stu-id="6a607-129">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="6a607-130">Dans des conditions normales, les emplacements de stockage des paramètres doivent être disponibles sur une connexion réseau rapide.</span><span class="sxs-lookup"><span data-stu-id="6a607-130">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="6a607-131">Le mode de liaison lente est uniquement exécuté de manière périodique.</span><span class="sxs-lookup"><span data-stu-id="6a607-131">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="6a607-132">Par défaut, la planification de la synchronisation du mode de liaison lente est définie sur toutes les 360 minutes.</span><span class="sxs-lookup"><span data-stu-id="6a607-132">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="6a607-133">Solution de contournement: pour modifier la fréquence de synchronisation en arrière-plan des ordinateurs en mode de liaison lente, vous pouvez configurer la stratégie de groupe pour la stratégie de synchronisation en arrière-plan pour les **fichiers en mode hors connexion**.</span><span class="sxs-lookup"><span data-stu-id="6a607-133">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="6a607-134">Les caractères spéciaux ne sont pas synchronisés</span><span class="sxs-lookup"><span data-stu-id="6a607-134">Special characters do not synchronize</span></span>

<span data-ttu-id="6a607-135">Certains caractères, tels que les symboles monétaires, ne sont pas synchronisés entre les ordinateurs Windows 7 et Windows 8 qui exécutent l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="6a607-135">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="6a607-136">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="6a607-136">WORKAROUND: None.</span></span>

### <span data-ttu-id="6a607-137">UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="6a607-137">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="6a607-138">Nous vous recommandons d’installer la version 32 bits de Microsoft Office pour les systèmes d’exploitation 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6a607-138">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="6a607-139">Pour choisir la version de Microsoft Office dont vous avez besoin, cliquez ici.</span><span class="sxs-lookup"><span data-stu-id="6a607-139">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="6a607-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="6a607-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="6a607-141">UE-V prend en charge les paramètres d’itinérance entre les différentes versions de l’architecture d’Office.</span><span class="sxs-lookup"><span data-stu-id="6a607-141">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="6a607-142">Par exemple, les paramètres d’Office 32 bits s’itinérance entre toutes les instances Office 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6a607-142">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="6a607-143">UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="6a607-143">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="6a607-144">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="6a607-144">WORKAROUND: None</span></span>

### <span data-ttu-id="6a607-145">Les autres dossiers du partage avec l’emplacement de stockage des paramètres ne sont pas disponibles en mode de connexion lente.</span><span class="sxs-lookup"><span data-stu-id="6a607-145">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="6a607-146">Les partages du magasin de valeurs doivent se trouver sur un partage réseau qui est utilisé pour les autres dossiers qui doivent toujours être disponibles.</span><span class="sxs-lookup"><span data-stu-id="6a607-146">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="6a607-147">Lorsque le partage réseau qui héberge l’emplacement de stockage des paramètres passe en mode de connexion lente, le seul dossier disponible est le dossier d’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="6a607-147">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="6a607-148">Les autres dossiers du partage ne sont pas disponibles en mode de connexion lente.</span><span class="sxs-lookup"><span data-stu-id="6a607-148">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="6a607-149">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="6a607-149">Workaround: None</span></span>

### <span data-ttu-id="6a607-150">Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants</span><span class="sxs-lookup"><span data-stu-id="6a607-150">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="6a607-151">Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants par la virtualisation de l’interface utilisateur et qui n’apparaissent pas à la première apparition des favoris sur un nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6a607-151">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="6a607-152">SOLUTION: favicons apparaît avec les favoris associés une fois que le signet est utilisé et mis en cache dans le navigateur Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6a607-152">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="6a607-153">Les chemins d’accès aux paramètres de fichier sont stockés dans le registre</span><span class="sxs-lookup"><span data-stu-id="6a607-153">File settings paths are stored in registry</span></span>

<span data-ttu-id="6a607-154">Certains paramètres d’application stockent les chemins d’accès de leurs fichiers de configuration et de paramètres en tant que valeurs dans le registre.</span><span class="sxs-lookup"><span data-stu-id="6a607-154">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="6a607-155">Les fichiers référencés sous forme de chemin d’accès dans le registre doivent être synchronisés lorsque les paramètres sont itinérants entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6a607-155">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="6a607-156">Solution de contournement: utilisez la redirection de dossiers ou d’autres technologies pour vous assurer que tous les fichiers référencés comme chemins d’accès aux paramètres de fichier sont présents et placés au même emplacement sur tous les ordinateurs dans lesquels les paramètres sont itinérants.</span><span class="sxs-lookup"><span data-stu-id="6a607-156">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="6a607-157">Les chemins de plus de 260 caractères ne sont pas pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a607-157">Paths longer than 260 characters are not supported</span></span>

<span data-ttu-id="6a607-158">Les chemins d’accès de stockage de paramètres de plus de 260 caractères ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6a607-158">Settings storage paths that are longer than 260 characters are not supported.</span></span> <span data-ttu-id="6a607-159">La copie des packages de paramètres d’UE-V vers des paramètres de stockage de paramètres de plus de 260 caractères échoue et génère le message d’exception suivant dans le journal des événements de fonctionnement d’UE-V: **\ [Booster:: FileSystem:: Copy \ _File: le système ne trouve pas le chemin d’accès indiqué**.</span><span class="sxs-lookup"><span data-stu-id="6a607-159">Copying the UE-V settings packages to settings storage paths that are longer than 260 characters will fail and generate the following exception message in the UE-V operational event log: **\[boost::filesystem::copy\_file: The system cannot find the path specified\]**.</span></span> <span data-ttu-id="6a607-160">Pour vérifier les événements du journal opérationnel, ouvrez l' **Observateur d’événements** et naviguez jusqu’à **applications et services consigne**le fonctionnement de l’enregistrement de la virtualisation de l'  /  **Microsoft**  /  **interface utilisateur**de Microsoft  /  **Logging**  /  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="6a607-160">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span>

<span data-ttu-id="6a607-161">Les chemins d’accès aux paramètres de fichiers de plus de 260 caractères ne sont pas pris en charge pour le moment.</span><span class="sxs-lookup"><span data-stu-id="6a607-161">File settings paths that are longer than 260 characters are not currently supported.</span></span> <span data-ttu-id="6a607-162">Les paramètres de fichiers référencés dans les modèles d’emplacement des paramètres de UE-V ne peuvent pas être situés dans un chemin d’accès de répertoire de plus de 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="6a607-162">File settings that are referenced in UE-V settings location templates cannot be located in a directory path that is longer than 260 characters.</span></span>

<span data-ttu-id="6a607-163">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="6a607-163">WORKAROUND: None.</span></span>

### <span data-ttu-id="6a607-164">UE-V agent retarde lors de la connexion ou de la connexion</span><span class="sxs-lookup"><span data-stu-id="6a607-164">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="6a607-165">Si une connexion ou une connexion se produit avant que les fichiers hors connexion n’aient déterminé qu’une liaison lente est en place, la déconnexion ou la connexion peuvent être retardées.</span><span class="sxs-lookup"><span data-stu-id="6a607-165">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="6a607-166">La fonctionnalité fichiers en mode hors connexion ne doit pas durer jusqu’à trois minutes pour détecter l’état actuel du réseau.</span><span class="sxs-lookup"><span data-stu-id="6a607-166">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="6a607-167">Si la connexion ou l’arrêt se produit avant que les fichiers hors connexion n’aient déterminé que l’ordinateur est connecté à une liaison lente, le package de paramètres d’UE-V sera envoyé au serveur au lieu du cache local.</span><span class="sxs-lookup"><span data-stu-id="6a607-167">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="6a607-168">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="6a607-168">WORKAROUND: None.</span></span>

### <span data-ttu-id="6a607-169">Conflit de paramètres lors de la tentative d’itinérance des paramètres du système d’exploitation sur Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a607-169">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="6a607-170">Dans Windows 8, si la synchronisation de compte Microsoft est activée avec UE-V pour les paramètres du système d’exploitation, les paramètres appliqués peuvent être incohérents.</span><span class="sxs-lookup"><span data-stu-id="6a607-170">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="6a607-171">Solution de contournement: effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="6a607-171">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="6a607-172">Désactiver la synchronisation des comptes Microsoft si vous utilisez UE-V pour itinérance dans les paramètres du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6a607-172">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="6a607-173">Désactiver UE-V pour les paramètres du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6a607-173">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="6a607-174">Certains paramètres du système d’exploitation ne suivent que les versions du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="6a607-174">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="6a607-175">Les paramètres du système d’exploitation pour le narrateur et les caractères de devise spécifiques aux paramètres régionaux ne seront itinérants que sur les versions de système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="6a607-175">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="6a607-176">Par exemple, les caractères monétaires ne seront déplacés que de Windows 7 vers Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a607-176">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="6a607-177">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="6a607-177">WORKAROUND: None</span></span>

### <span data-ttu-id="6a607-178">Les signets Internet Explorer n’apparaissent pas dans Internet Explorer Smartbar</span><span class="sxs-lookup"><span data-stu-id="6a607-178">Internet Explorer bookmarks do not appear in the Internet Explorer smartbar</span></span>

<span data-ttu-id="6a607-179">Lorsque Internet Explorer est en déplacement entre deux ordinateurs, l’index sur le second ordinateur ne peut pas être mis à jour, donc lorsque vous tapez dans la barre d’adresses, les favoris ne s’afficheront pas sous la forme d’un résultat de recherche sur l’ordinateur 2.</span><span class="sxs-lookup"><span data-stu-id="6a607-179">When Internet Explorer bookmarks roam from one computer to another computer, the index on the second computer cannot update, so when typing in the address bar, the favorite will not appear as a possible search result on computer 2.</span></span>

<span data-ttu-id="6a607-180">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="6a607-180">WORKAROUND: None</span></span>

 

 





