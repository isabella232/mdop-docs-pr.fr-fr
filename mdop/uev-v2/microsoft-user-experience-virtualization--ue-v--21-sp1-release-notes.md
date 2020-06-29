---
title: Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1SP1
description: Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1SP1
author: dansimp
ms.assetid: 561988c4-cc5c-4e15-970b-16e942c8f2ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/30/2017
ms.openlocfilehash: 974914421c61c829b5a32e336bddf8ea1addf514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811213"
---
# <span data-ttu-id="e7cdd-103">Notes de publication pour Microsoft User Experience Virtualization (UE-V)2.1SP1</span><span class="sxs-lookup"><span data-stu-id="e7cdd-103">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>


<span data-ttu-id="e7cdd-104">Pour effectuer une recherche dans les notes de publication de Microsoft User interface 2,1 SP1, appuyez sur Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-104">To search Microsoft User Experience Virtualization 2.1 SP1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="e7cdd-105">Nous vous conseillons de lire soigneusement ces notes de publication avant d’installer UE-V.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="e7cdd-106">Les notes de publication contiennent des informations nécessaires à l’installation réussie de la virtualisation de l’interface utilisateur et contiennent des informations supplémentaires qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="e7cdd-107">S’il existe des différences entre ces notes de publication et d’autres documents UE-V, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="e7cdd-108">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="e7cdd-109">Envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="e7cdd-109">Providing feedback</span></span>


<span data-ttu-id="e7cdd-110">Dites-nous ce que vous pensez de notre documentation pour MDOP en nous fournissant vos commentaires et commentaires.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="e7cdd-111">Envoyez votre commentaires de documentation à [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="e7cdd-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="e7cdd-112">UE-V problèmes connus</span><span class="sxs-lookup"><span data-stu-id="e7cdd-112">UE-V known issues</span></span>


<span data-ttu-id="e7cdd-113">Cette section contient des notes de publication relatives à l’utilisation de User Virtualization 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-113">This section contains release notes for User Experience Virtualization 2.1 SP1.</span></span>

### <span data-ttu-id="e7cdd-114">Les modèles d’emplacement des paramètres d’UE-V peuvent provoquer le blocage de Skype</span><span class="sxs-lookup"><span data-stu-id="e7cdd-114">UE-V settings location templates for Skype cause Skype to crash</span></span>

<span data-ttu-id="e7cdd-115">Lorsqu’un utilisateur génère un modèle d’emplacement des paramètres valide pour l’application de bureau Skype, le inscrit, puis lance l’application de bureau Skype, Skype se bloque.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-115">When a user generates a valid settings location template for the Skype desktop application, registers it, and then launches the Skype desktop application, Skype crashes.</span></span> <span data-ttu-id="e7cdd-116">Un accès \ _VIOLATION est enregistré dans le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-116">An ACCESS\_VIOLATION is recorded in the Application Event Log.</span></span>

<span data-ttu-id="e7cdd-117">Solution de contournement: supprimez ou annulez l’enregistrement du modèle Skype pour permettre à Skype de fonctionner de nouveau.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-117">WORKAROUND: Remove or unregister the Skype template to allow Skype to work again.</span></span>

### <span data-ttu-id="e7cdd-118">Les scripts existants pour les installations silencieuses de UE-V peuvent échouer</span><span class="sxs-lookup"><span data-stu-id="e7cdd-118">Existing scripts for silent installations of UE-V may fail</span></span>

<span data-ttu-id="e7cdd-119">Deux modifications apportées au programme d’installation d’UE-V peuvent entraîner l’échec des scripts d’installation en mode silencieux qui fonctionnaient dans les versions précédentes d’UE-v lors de l’installation d’UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-119">Two changes made to the UE-V installer can cause silent installation scripts that worked for previous versions of UE-V to fail when installing UE-V 2.1 SP1.</span></span> <span data-ttu-id="e7cdd-120">Le premier est une nouvelle obligation pour les utilisateurs d’accepter les termes du contrat de licence et d’accepter ou de refuser la participation au programme d’amélioration du produit, même pendant une installation silencieuse.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-120">The first is a new requirement that users must accept the license terms and agree to or decline participation in the Customer Experience Improvement Program (CEIP), even during a silent installation.</span></span> <span data-ttu-id="e7cdd-121">L’utilisation du paramètre/q n’est plus suffisante pour indiquer l’acceptation des termes du contrat de licence et du contrat de participation au programme d’amélioration du produit.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-121">Using the /q parameter is no longer sufficient to indicate acceptance of the license terms and agreement to participate in CEIP.</span></span>

<span data-ttu-id="e7cdd-122">Deuxièmement, le programme d’installation force désormais le redémarrage de l’ordinateur après l’installation de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-122">Second, the installer now forces a computer restart after installing the UE-V Agent.</span></span> <span data-ttu-id="e7cdd-123">Cela peut entraîner l’échec d’un script d’installation s’il n’attend pas le redémarrage (par exemple, il installe d’abord l’agent UE-V, puis installe immédiatement le générateur).</span><span class="sxs-lookup"><span data-stu-id="e7cdd-123">This can cause an install script to fail if it is not expecting the restart (for example, it installs the UE-V Agent first and then immediately installs the generator).</span></span>

<span data-ttu-id="e7cdd-124">SOLUTION: le programme d’installation d’UE-V (. msi) comporte deux nouveaux paramètres de ligne de commande qui prennent en charge les installations silencieuses.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-124">WORKAROUND: The UE-V installer (.msi) has two new command-line parameters that support silent installations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e7cdd-125">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e7cdd-125">Parameter</span></span></th>
<th align="left"><span data-ttu-id="e7cdd-126">Description</span><span class="sxs-lookup"><span data-stu-id="e7cdd-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e7cdd-127">/ACCEPTLICENSETERMS = true</span><span class="sxs-lookup"><span data-stu-id="e7cdd-127">/ACCEPTLICENSETERMS=True</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-128">Définissez ce paramètre sur <strong> true </strong> pour installer UE-V en silence.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-128">Set this parameter to <strong>True</strong> to install UE-V silently.</span></span> <span data-ttu-id="e7cdd-129">L’ajout de ce paramètre implique que l’utilisateur accepte les termes du contrat de licence UE-V, qui sont trouvés (par défaut) ici:%ProgramFiles%\Microsoft user interface Virtualization\Agent</span><span class="sxs-lookup"><span data-stu-id="e7cdd-129">Adding this parameter implies that the user accepts the UE-V license terms, which are found (by default) here: %ProgramFiles%\Microsoft User Experience Virtualization\Agent</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e7cdd-130">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="e7cdd-130">/NORESTART</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-131">Ce paramètre empêche le redémarrage obligatoire après l’installation d’UE-V agent.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-131">This parameter prevents the mandatory restart after the UE-V agent is installed.</span></span> <span data-ttu-id="e7cdd-132">Le code de retour 3010 indique qu’un redémarrage est nécessaire avant d’utiliser UE-V.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-132">A return code of 3010 indicates that a restart is required prior to using UE-V.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="e7cdd-133">Les paramètres de registre ne sont pas synchronisés entre App-V et les applications natives sur le même ordinateur</span><span class="sxs-lookup"><span data-stu-id="e7cdd-133">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="e7cdd-134">Lorsqu’un ordinateur dispose d’une application installée par le biais de la virtualisation des applications (App-V) et en local avec un fichier Windows Installer (. msi), les paramètres basés sur le registre ne sont pas synchronisés entre les technologies.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-134">When a computer has an application that is installed through both Application Virtualization (App-V) and locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="e7cdd-135">SOLUTION: pour résoudre ce problème, exécutez l’application en sélectionnant l’une des deux technologies, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-135">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="e7cdd-136">Résultats inattendus avec Office 2010 et Office 2013 installés</span><span class="sxs-lookup"><span data-stu-id="e7cdd-136">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="e7cdd-137">Lorsqu’un utilisateur a installé Office 2010 et Office 2013, tous les paramètres courants entre les deux versions d’Office sont itinérants par UE-V.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-137">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="e7cdd-138">Cela risque de rendre la taille du package Office 2010 trop importante ou engendrer des conflits inattendus avec 2013, en particulier si la version d’Office 365 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-138">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="e7cdd-139">Solution de contournement: installez une seule version d’Office ou limitez les paramètres qui sont synchronisés par UE-V.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-139">WORKAROUND: Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="e7cdd-140">La désinstallation de l’application Windows 8 rétablit les paramètres à l’état initial</span><span class="sxs-lookup"><span data-stu-id="e7cdd-140">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="e7cdd-141">Lors de l’utilisation de la synchronisation des paramètres d’UE-V pour une application Windows 8, si l’utilisateur désinstalle l’application, puis réinstalle l’application, les paramètres de l’application rétablissent leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-141">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="e7cdd-142">Ce problème se produit car la désinstallation supprime la copie locale (mise en cache) des paramètres de l’application, mais ne supprime pas le package de paramètres UE-V local.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-142"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="e7cdd-143">Lorsque l’application est réinstallée et lancée, UE-V rassemblez les paramètres d’application qui ont été réinitialisés aux valeurs par défaut de l’application, puis chargez les paramètres par défaut sur l’emplacement de stockage central.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-143"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="e7cdd-144">D’autres ordinateurs exécutant l’application téléchargent les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-144"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="e7cdd-145">Ce comportement est identique au comportement des applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-145"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="e7cdd-146">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-146">WORKAROUND: None.</span></span>

### <span data-ttu-id="e7cdd-147">UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="e7cdd-147">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="e7cdd-148">Nous vous recommandons d’installer la version 32 bits de Microsoft Office pour les systèmes d’exploitation 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-148">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="e7cdd-149">Pour choisir la version de Microsoft Office dont vous avez besoin, cliquez ici.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-149">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="e7cdd-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="e7cdd-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="e7cdd-151">UE-V prend en charge les paramètres d’itinérance entre les différentes versions de l’architecture d’Office.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-151">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="e7cdd-152">Par exemple, les paramètres d’Office 32 bits s’itinérance entre toutes les instances Office 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-152">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="e7cdd-153">UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-153">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="e7cdd-154">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="e7cdd-154">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="e7cdd-155">Les MSI ne sont pas localisés</span><span class="sxs-lookup"><span data-stu-id="e7cdd-155">MSI’s are not localized</span></span>

<span data-ttu-id="e7cdd-156">UE-V inclut un programme d’installation localisé pour les agents UE-V et UE-V.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-156">UE-V includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="e7cdd-157">Ils sont toujours disponibles, mais l’interface utilisateur est réduite et l’affichage du MSI uniquement en anglais.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-157">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="e7cdd-158">Malgré le fichier en anglais, le programme d’installation installe toutes les langues prises en charge lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-158">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="e7cdd-159">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="e7cdd-159">WORKAROUND: None</span></span>

### <span data-ttu-id="e7cdd-160">Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants</span><span class="sxs-lookup"><span data-stu-id="e7cdd-160">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="e7cdd-161">Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants par la virtualisation de l’interface utilisateur et qui n’apparaissent pas à la première apparition des favoris sur un nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-161">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="e7cdd-162">SOLUTION: favicons apparaît avec les favoris associés une fois que le signet est utilisé et mis en cache dans le navigateur Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-162">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="e7cdd-163">Les chemins d’accès aux paramètres de fichier sont stockés dans le registre</span><span class="sxs-lookup"><span data-stu-id="e7cdd-163">File settings paths are stored in registry</span></span>

<span data-ttu-id="e7cdd-164">Certains paramètres d’application stockent les chemins d’accès de leurs fichiers de configuration et de paramètres en tant que valeurs dans le registre.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-164">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="e7cdd-165">Les fichiers référencés sous forme de chemin d’accès dans le registre doivent être synchronisés lorsque les paramètres sont itinérants entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-165">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="e7cdd-166">Solution de contournement: utilisez la redirection de dossiers ou d’autres technologies pour vous assurer que tous les fichiers référencés comme chemins d’accès aux paramètres de fichier sont présents et placés au même emplacement sur tous les ordinateurs dans lesquels les paramètres sont itinérants.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-166">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="e7cdd-167">Les chemins de stockage de paramètres longs peuvent générer une erreur</span><span class="sxs-lookup"><span data-stu-id="e7cdd-167">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="e7cdd-168">Le raccourci de stockage des paramètres reste le plus court possible.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-168">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="e7cdd-169">Les chemins longs peuvent empêcher la résolution ou la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-169">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="e7cdd-170">UE-V utilise le chemin de stockage des paramètres dans le cadre du chemin d’accès calculé au stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-170">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="e7cdd-171">Ce chemin d’accès est calculé comme suit: Path Storage path + "settingspackages" + package dir (ID de modèle) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-171">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="e7cdd-172">Si le chemin d’accès calculé est supérieur à 260 caractères, le stockage du package échoue et génère le message d’erreur suivant dans le journal des événements de fonctionnement d’UE-V:</span><span class="sxs-lookup"><span data-stu-id="e7cdd-172">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="e7cdd-173">Pour vérifier les événements du journal opérationnel, ouvrez l’observateur d’événements et naviguez jusqu’à la section journaux des applications et des services/Microsoft/User-Virtualization/Logging/Operations.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-173">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="e7cdd-174">Solution de contournement: aucune.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-174">WORKAROUND: None.</span></span>

### <span data-ttu-id="e7cdd-175">Certains paramètres du système d’exploitation ne suivent que les versions du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e7cdd-175">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="e7cdd-176">Les paramètres du système d’exploitation pour le narrateur et les caractères de devise spécifiques aux paramètres régionaux (par exemple, les paramètres linguistiques et régionaux) ne sont itinérants que sur les versions de système d’exploitation de Windows.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-176">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="e7cdd-177">Par exemple, les caractères monétaires ne seront pas itinérants entre Windows 7 et Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-177">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="e7cdd-178">Solution de contournement: aucune</span><span class="sxs-lookup"><span data-stu-id="e7cdd-178">WORKAROUND: None</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="e7cdd-179">UE-V 1 agent génère des erreurs lors de l’exécution de modèles UE-V 2</span><span class="sxs-lookup"><span data-stu-id="e7cdd-179">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="e7cdd-180">Si un modèle d’emplacement des paramètres d’UE-V 2 est distribué sur un ordinateur installé avec un agent UE-V 1, certains paramètres ne sont pas synchronisés entre les ordinateurs et l’agent signale les erreurs dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-180">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="e7cdd-181">Solution de contournement: lorsque vous migrez d’UE-V 1 vers UE-V 2 et qu’il est probable que des ordinateurs exécutent la version précédente de l’agent, vous devez créer un catalogue UE-V 2. x distinct pour prendre en charge l’agent et les modèles UE-V 2. x.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-181">WORKAROUND: When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.x catalog to support the UE-V 2.x Agent and templates.</span></span>

### <span data-ttu-id="e7cdd-182">Retard de la fermeture de session UE-V</span><span class="sxs-lookup"><span data-stu-id="e7cdd-182">UE-V logoff delay</span></span>

<span data-ttu-id="e7cdd-183">Occasionnellement lors de la fermeture de session, UE-V met trop de temps à synchroniser les paramètres.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-183">Occasionally on logoff, UE-V takes a long time to sync settings.</span></span> <span data-ttu-id="e7cdd-184">En règle générale, il s’agit d’un réseau à forte latence ou d’une utilisation incorrecte du système de fichiers Distrubuted.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-184">Typically, this is due to a high latency network or incorrect use of Distrubuted File System (DFS).</span></span>
<span data-ttu-id="e7cdd-185">Pour la prise en charge du système de fichiers DFS, consultez [l’instruction de support de Microsoft concernant les données de profil utilisateur répliquées](https://support.microsoft.com/kb/2533009) pour obtenir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-185">For DFS support, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://support.microsoft.com/kb/2533009) for further details.</span></span>

<span data-ttu-id="e7cdd-186">Solution de contournement: à partir de HF03, une nouvelle clé de registre a été ajoutée la clé de Registre suivante fournit un mécanisme selon lequel le délai de déconnexion maximal peut être spécifié \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval</span><span class="sxs-lookup"><span data-stu-id="e7cdd-186">WORKAROUND: Starting with HF03, a new registry key has been introduced The following registry key provides a mechanism by which the maximum logoff delay can be specified \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval</span></span>

<span data-ttu-id="e7cdd-187">Pour plus d’informations [, voir paramètres de Registre UE-V](https://support.microsoft.com/kb/2770042) .</span><span class="sxs-lookup"><span data-stu-id="e7cdd-187">See [UE-V registry settings](https://support.microsoft.com/kb/2770042) for further details</span></span>

## <span data-ttu-id="e7cdd-188">HotFix et Articles de la base de connaissances pour UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="e7cdd-188">Hotfixes and Knowledge Base articles for UE-V 2.1 SP1</span></span>


<span data-ttu-id="e7cdd-189">Cette section contient des correctifs et des Articles de la base de connaissances pour UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-189">This section contains hotfixes and KB articles for UE-V 2.1 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="e7cdd-190">Article de la base de connaissances</span><span class="sxs-lookup"><span data-stu-id="e7cdd-190">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="e7cdd-191">Title</span><span class="sxs-lookup"><span data-stu-id="e7cdd-191">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="e7cdd-192">Link</span><span class="sxs-lookup"><span data-stu-id="e7cdd-192">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7cdd-193">3018608</span><span class="sxs-lookup"><span data-stu-id="e7cdd-193">3018608</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-194">UE-V 2,1-TemplateConsole.exe se bloque lorsque les classes WMI UE-V sont manquantes</span><span class="sxs-lookup"><span data-stu-id="e7cdd-194">UE-V 2.1 - TemplateConsole.exe crashes when UE-V WMI classes are missing</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)"><span data-ttu-id="e7cdd-195">support.microsoft.com/kb/3018608/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-195">support.microsoft.com/kb/3018608/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7cdd-196">2903501</span><span class="sxs-lookup"><span data-stu-id="e7cdd-196">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-197">UE-V: compatibilité entre les utilisateurs et la virtualisation de l’interface utilisateur avec les profils utilisateur</span><span class="sxs-lookup"><span data-stu-id="e7cdd-197">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="e7cdd-198">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-198">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7cdd-199">2770042</span><span class="sxs-lookup"><span data-stu-id="e7cdd-199">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-200">Paramètres de Registre UE-V</span><span class="sxs-lookup"><span data-stu-id="e7cdd-200">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="e7cdd-201">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-201">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7cdd-202">2847017</span><span class="sxs-lookup"><span data-stu-id="e7cdd-202">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-203">Paramètres d’UE-V répliqués par Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="e7cdd-203">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="e7cdd-204">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-204">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7cdd-205">2769631</span><span class="sxs-lookup"><span data-stu-id="e7cdd-205">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-206">Réparation d’une installation d’UE-V endommagée</span><span class="sxs-lookup"><span data-stu-id="e7cdd-206">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="e7cdd-207">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-207">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7cdd-208">2850989</span><span class="sxs-lookup"><span data-stu-id="e7cdd-208">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-209">La migration de profils MAPI avec Microsoft UE-V n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e7cdd-209">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="e7cdd-210">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-210">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7cdd-211">2769586</span><span class="sxs-lookup"><span data-stu-id="e7cdd-211">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-212">UE-V: itinérance de dossiers et de clés de Registre vides</span><span class="sxs-lookup"><span data-stu-id="e7cdd-212">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="e7cdd-213">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-213">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7cdd-214">2782997</span><span class="sxs-lookup"><span data-stu-id="e7cdd-214">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-215">Comment activer la journalisation de débogage dans Microsoft User Interface Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="e7cdd-215">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="e7cdd-216">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-216">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7cdd-217">2769570</span><span class="sxs-lookup"><span data-stu-id="e7cdd-217">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-218">UE-V ne met pas à jour le thème pour les sessions RDS ou VDI</span><span class="sxs-lookup"><span data-stu-id="e7cdd-218">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="e7cdd-219">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-219">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7cdd-220">2850582</span><span class="sxs-lookup"><span data-stu-id="e7cdd-220">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-221">Utiliser la virtualisation de l’utilisation de Microsoft avec les applications App-V</span><span class="sxs-lookup"><span data-stu-id="e7cdd-221">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="e7cdd-222">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-222">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7cdd-223">3041879</span><span class="sxs-lookup"><span data-stu-id="e7cdd-223">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-224">Versions de fichiers actuelles pour l’utilisation de Microsoft User-virtualisation</span><span class="sxs-lookup"><span data-stu-id="e7cdd-224">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="e7cdd-225">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-225">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7cdd-226">2843592</span><span class="sxs-lookup"><span data-stu-id="e7cdd-226">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7cdd-227">Informations sur la virtualisation et la disponibilité des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e7cdd-227">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="e7cdd-228">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="e7cdd-228">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 






 

 





