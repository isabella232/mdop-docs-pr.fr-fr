---
title: Nouveautés dans App-V5.0
description: Nouveautés dans App-V5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804813"
---
# <span data-ttu-id="7586f-103">Nouveautés dans App-V5.0</span><span class="sxs-lookup"><span data-stu-id="7586f-103">What's New in App-V 5.0</span></span>


<span data-ttu-id="7586f-104">Cette section s’utilise pour les utilisateurs qui connaissent déjà App-V et qui souhaitent savoir ce qui a changé dans l’app-v 5,0 si vous ne connaissez pas encore l’application-v, vous devez commencer par lire [planification pour App-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="7586f-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="7586f-105">Modifications apportées aux fonctionnalités standard</span><span class="sxs-lookup"><span data-stu-id="7586f-105">Changes in Standard Functionality</span></span>


<span data-ttu-id="7586f-106">Les sections suivantes contiennent des informations sur les modifications apportées aux fonctionnalités standard pour App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-106">The following sections contain information about the changes in standard functionality for App-V 5.0.</span></span>

### <span data-ttu-id="7586f-107">Modifications apportées aux systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="7586f-107">Changes to Supported Operating Systems</span></span>

<span data-ttu-id="7586f-108">Pour plus d’informations, voir [configurations App-V 5,0 prises en charge](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7586f-108">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

## <span data-ttu-id="7586f-109">Modifications apportées au Sequencer</span><span class="sxs-lookup"><span data-stu-id="7586f-109">Changes to the sequencer</span></span>


<span data-ttu-id="7586f-110">Les sections suivantes contiennent des informations sur les modifications apportées au Sequencer App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-110">The following sections contain information about the changes in the App-V 5.0 sequencer.</span></span>

### <span data-ttu-id="7586f-111">Modification spécifique au Sequencer</span><span class="sxs-lookup"><span data-stu-id="7586f-111">Specific change to the sequencer</span></span>

<span data-ttu-id="7586f-112">Le tableau suivant contient des informations sur les modifications apportées avec le Sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7586f-112">The following table displays information about what has changed with the App-V 5.0 sequencer</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7586f-113">Fonction Sequencer</span><span class="sxs-lookup"><span data-stu-id="7586f-113">Sequencer Feature</span></span></th>
<th align="left"><span data-ttu-id="7586f-114">Fonctionnalité Sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="7586f-114">App-V 5.0 Sequencer Functionality</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7586f-115">Traitement du redémarrage</span><span class="sxs-lookup"><span data-stu-id="7586f-115">Reboot processing</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-116">Lorsqu’une application vous invite à redémarrer, vous devez autoriser l’application à redémarrer l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="7586f-116">When an application prompts for a restart, you should allow the application to restart the computer running the sequencer.</span></span> <span data-ttu-id="7586f-117">L’ordinateur exécutant le Sequencer redémarre et le Sequencer reprend en mode d’analyse.</span><span class="sxs-lookup"><span data-stu-id="7586f-117">The computer running the sequencer will restart and the sequencer will resume in monitoring mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7586f-118">Spécification du répertoire d’application virtuel</span><span class="sxs-lookup"><span data-stu-id="7586f-118">Specifying the virtual application directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-119">Le répertoire d’application virtuel est un paramètre obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7586f-119">Virtual Application Directory is a mandatory parameter.</span></span> <span data-ttu-id="7586f-120">Pour obtenir de meilleurs résultats, il doit correspondre au répertoire d’installation du programme d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="7586f-120">For best results, it should match the installation directory of the application installer.</span></span> <span data-ttu-id="7586f-121">Cela a pour effet d’optimiser les performances et la compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="7586f-121">This results in more optimal performance and application compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7586f-122">Modification des raccourcis/FTAs</span><span class="sxs-lookup"><span data-stu-id="7586f-122">Editing shortcuts/FTAs</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-123">La page raccourcis/FTA s’affiche sur <strong> la </strong> page modification avancée une fois l’Assistant séquençage terminé.</span><span class="sxs-lookup"><span data-stu-id="7586f-123">The Shortcuts/FTA page is on the <strong>Advanced</strong> editing page after the sequencing wizard has completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7586f-124">Onglet Historique des modifications</span><span class="sxs-lookup"><span data-stu-id="7586f-124">Change History Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-125">L’onglet historique des modifications a été supprimé pour App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-125">The Change History tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7586f-126">Onglet OSD</span><span class="sxs-lookup"><span data-stu-id="7586f-126">OSD Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-127">L’onglet OSD a été supprimé pour App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-127">The OSD tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7586f-128">Onglet Services virtuels</span><span class="sxs-lookup"><span data-stu-id="7586f-128">Virtual Services Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-129">L’onglet services virtuels a été supprimé pour App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-129">The virtual services tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7586f-130">Onglet fichiers/système de fichiers virtuel</span><span class="sxs-lookup"><span data-stu-id="7586f-130">Files/Virtual File System Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-131">Ces onglets sont combinés et vous permettent de modifier les fichiers de package.</span><span class="sxs-lookup"><span data-stu-id="7586f-131">These tabs are combined and allow you to modify package files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7586f-132">Onglet Déploiement</span><span class="sxs-lookup"><span data-stu-id="7586f-132">Deployment Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-133">Il n’existe plus d’options de configuration de l’URL du serveur dans les packages.</span><span class="sxs-lookup"><span data-stu-id="7586f-133">There are no longer options to configure the server URL in the packages.</span></span> <span data-ttu-id="7586f-134">À présent, vous devez configurer cette opération à l’aide de la configuration de déploiement ou du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7586f-134">You should configure this now using deployment configuration, or the management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7586f-135">Outil convertisseur de package</span><span class="sxs-lookup"><span data-stu-id="7586f-135">Package Converter Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-136">Vous pouvez désormais utiliser PowerShell pour convertir des packages créés dans des versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="7586f-136">You can now use PowerShell to convert packages created in previous versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7586f-137">Module complémentaire/middleware</span><span class="sxs-lookup"><span data-stu-id="7586f-137">Add-on/Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-138">Vous pouvez développer des packages parents lors du séquençage d’une application de complément ou middleware.</span><span class="sxs-lookup"><span data-stu-id="7586f-138">You can expand parent packages when you are sequencing an Add-On or Middleware application.</span></span> <span data-ttu-id="7586f-139">Les modules complémentaires et les packages middleware doivent être connectés à l’aide de groupes de connexion dans l’application-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-139">Add-ons and Middleware packages must be connected using connection groups in App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7586f-140">Sortie de fichiers</span><span class="sxs-lookup"><span data-stu-id="7586f-140">Files output</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-141">Les fichiers suivants sont créés à l’aide de App-V 5,0, du programme d’installation Windows (. msi), de la configuration du déploiement, de la configuration utilisateur et du Report.XML.</span><span class="sxs-lookup"><span data-stu-id="7586f-141">The following files are created with App-V 5.0, Windows Installer (.msi), .appv, deployment configuration, user configuration, and the Report.XML.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7586f-142">Packages de compression/de sécurité/packages MSI</span><span class="sxs-lookup"><span data-stu-id="7586f-142">Compression/Security descriptors/MSI packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-143">La compression et la création d’un fichier Windows Installer (. msi) s’exécutent automatiquement pour tous les packages et vous ne pouvez plus remplacer les descripteurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7586f-143">Compression and the creation of a Windows Installer (.msi) file are automatic for all packages and you can no longer override security descriptors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7586f-144">Outils/options</span><span class="sxs-lookup"><span data-stu-id="7586f-144">Tools / Options</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-145">La fenêtre Diagnostics a été supprimée ainsi que d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="7586f-145">The Diagnostics window has been removed as well as several other settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7586f-146">Lecteur d’installation</span><span class="sxs-lookup"><span data-stu-id="7586f-146">Installation Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-147">Un lecteur d’installation n’est plus nécessaire lorsque vous installez une application.</span><span class="sxs-lookup"><span data-stu-id="7586f-147">An installation drive is no longer required when you install an application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7586f-148">Flux OOS</span><span class="sxs-lookup"><span data-stu-id="7586f-148">OOS Streaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="7586f-149">S’il n’y a pas d’optimisation de flux, les packages sont défectueux lorsque ceux-ci sont invités par des ordinateurs exécutant le client App-V 5,0 jusqu’à ce qu’ils puissent lancer.</span><span class="sxs-lookup"><span data-stu-id="7586f-149">If no stream optimization is performed, packages are stream faulted when they are requested by computers running the App-V 5.0 client until they can launch.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7586f-150">Q: &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="7586f-150">Q:&lt;/p&gt;</span></span></td>
<td align="left"><p><span data-ttu-id="7586f-151">App-V 5,0 utilise le système de fichiers natif et ne nécessite plus de Q:.</span><span class="sxs-lookup"><span data-stu-id="7586f-151">App-V 5.0 uses the native file system and no longer requires a Q:.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7586f-152">Détection des erreurs de séquençage</span><span class="sxs-lookup"><span data-stu-id="7586f-152">Sequencing error detection</span></span>


<span data-ttu-id="7586f-153">Le Sequencer App-V 5,0 peut détecter les problèmes courants de séquençage lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="7586f-153">The App-V 5.0 sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="7586f-154">La page **rapport d’installation** à la fin de l’Assistant séquençage affiche les messages de diagnostic classés en **erreurs**, **avertissements**et **informations** en fonction de la gravité du problème.</span><span class="sxs-lookup"><span data-stu-id="7586f-154">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="7586f-155">Pour afficher des informations plus détaillées sur un événement, double-cliquez sur l’élément que vous souhaitez consulter dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="7586f-155">To display more detailed information about an event, double-click the item you want to review in the report.</span></span> <span data-ttu-id="7586f-156">Les problèmes de séquençage, ainsi que des suggestions sur la façon de résoudre les problèmes, sont affichées.</span><span class="sxs-lookup"><span data-stu-id="7586f-156">The sequencing issues, as well as suggestions about how to resolve the issues are displayed.</span></span> <span data-ttu-id="7586f-157">Les informations issues du rapport de préparation du système et du rapport d’installation sont synthétisées lorsque vous avez terminé la création d’un package.</span><span class="sxs-lookup"><span data-stu-id="7586f-157">Information from the system preparation report and the installation report are summarized when you have finished creating a package.</span></span> <span data-ttu-id="7586f-158">La liste suivante indique les types de problèmes disponibles dans le rapport:</span><span class="sxs-lookup"><span data-stu-id="7586f-158">The following list displays the types of issues available in the report:</span></span>

-   <span data-ttu-id="7586f-159">Fichiers exclus.</span><span class="sxs-lookup"><span data-stu-id="7586f-159">Excluded files.</span></span>

-   <span data-ttu-id="7586f-160">Informations sur le pilote.</span><span class="sxs-lookup"><span data-stu-id="7586f-160">Driver information.</span></span>

-   <span data-ttu-id="7586f-161">Différences du système COM+.</span><span class="sxs-lookup"><span data-stu-id="7586f-161">COM+ system differences.</span></span>

-   <span data-ttu-id="7586f-162">Conflits côte à côte (SxS).</span><span class="sxs-lookup"><span data-stu-id="7586f-162">Side-by-side (SxS) conflicts.</span></span>

-   <span data-ttu-id="7586f-163">Extensions Shell.</span><span class="sxs-lookup"><span data-stu-id="7586f-163">Shell Extensions.</span></span>

-   <span data-ttu-id="7586f-164">Informations sur les services non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7586f-164">Information about unsupported services.</span></span>

-   <span data-ttu-id="7586f-165">Protocole.</span><span class="sxs-lookup"><span data-stu-id="7586f-165">DCOM.</span></span>

## <span data-ttu-id="7586f-166">Groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="7586f-166">Connection Groups</span></span>


<span data-ttu-id="7586f-167">La fonctionnalité App-V auparavant appelée **composition suite dynamique** est désormais désignée sous le nom de **groupes de connexion** dans App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-167">The App-V feature formerly known as **Dynamic Suite Composition** is now referred to as **Connection Groups** in App-V 5.0.</span></span> <span data-ttu-id="7586f-168">Pour plus d’informations sur l’utilisation des groupes de connexion, voir [gestion des groupes de connexion](managing-connection-groups.md).</span><span class="sxs-lookup"><span data-stu-id="7586f-168">For more information about using Connection Groups see [Managing Connection Groups](managing-connection-groups.md).</span></span>

## <span data-ttu-id="7586f-169">Fonctionnalité de gestion des licences et de mesure</span><span class="sxs-lookup"><span data-stu-id="7586f-169">Licensing and Metering Functionality</span></span>


<span data-ttu-id="7586f-170">La fonctionnalité d’application et de gestion des licences a été supprimée dans App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-170">The application and licensing functionality has been removed in App-V 5.0.</span></span> <span data-ttu-id="7586f-171">Le positionnement réel des licences dans votre environnement dépend des droits de licence et d’utilisation de votre logiciel spécifiques accordés par les termes du contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="7586f-171">The actual license positions in your environment depend on the specific software title license and usage rights granted by the associated license terms.</span></span>

## <span data-ttu-id="7586f-172">Cache de fichiers et d’applications</span><span class="sxs-lookup"><span data-stu-id="7586f-172">File and Application Cache</span></span>


<span data-ttu-id="7586f-173">Il n’y a pas de cache de fichiers ou d’application disponible avec App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7586f-173">There is no file or application cache available with App-V 5.0.</span></span>






## <span data-ttu-id="7586f-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7586f-174">Related topics</span></span>


[<span data-ttu-id="7586f-175">À propos d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="7586f-175">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





