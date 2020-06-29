---
title: À propos d'App-V5.0 SP2
description: À propos d'App-V5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806126"
---
# <span data-ttu-id="a4ba6-103">À propos d'App-V5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="a4ba6-103">About App-V 5.0 SP2</span></span>


<span data-ttu-id="a4ba6-104">App-V 5.0 SP2 fournit une plateforme intégrée améliorée, une virtualisation plus flexible et une gestion puissante des applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-104">App-V 5.0SP2 provides an improved integrated platform, more flexible virtualization, and powerful management for virtualized applications.</span></span> <span data-ttu-id="a4ba6-105">Pour plus d’informations, voir [vue d’ensemble de l’application-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .</span><span class="sxs-lookup"><span data-stu-id="a4ba6-105">For more information see, [App-V 5.0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) (https://go.microsoft.com/fwlink/?LinkId=325265).</span></span>

## <span data-ttu-id="a4ba6-106">Modifications apportées aux fonctionnalités standard App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="a4ba6-106">Changes in Standard App-V 5.0SP2 Functionality</span></span>


<span data-ttu-id="a4ba6-107">Les sections suivantes contiennent des informations sur les modifications apportées aux fonctionnalités standard pour App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-107">The following sections contain information about the changes in standard functionality for App-V 5.0SP2.</span></span>

### <a href="" id="bkmk-sp2-supported-cfg"></a><span data-ttu-id="a4ba6-108">Prise en charge de Windows Server 2012 R2 et Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="a4ba6-108">Support for Windows Server 2012 R2 and Windows 8.1</span></span>

<span data-ttu-id="a4ba6-109">App-V 5,0 prend en charge Windows Server 2012 R2 et Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="a4ba6-109">App-V 5.0 includes support for Windows Server 2012 R2 and Windows 8.1</span></span>

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> <span data-ttu-id="a4ba6-110">App-V 5.0 SP2 prend désormais en charge la redirection de dossiers pour le répertoire AppData d’itinérance de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-110">App-V 5.0SP2 now supports folder redirection for the user’s roaming AppData directory</span></span>

<span data-ttu-id="a4ba6-111">App-V 5.0 SP2 prend en charge l’itinérance. redirection de dossier.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-111">App-V 5.0SP2 supports roaming AppData (%AppData%) folder redirection.</span></span> <span data-ttu-id="a4ba6-112">Pour plus d’informations, reportez-vous [à la planification de l’utilisation de la redirection de dossiers avec App-V](planning-to-use-folder-redirection-with-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="a4ba6-112">For more information, see the [Planning to Use Folder Redirection with App-V](planning-to-use-folder-redirection-with-app-v.md).</span></span>

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a><span data-ttu-id="a4ba6-113">Améliorations de la mise à niveau du package et des tâches en attente</span><span class="sxs-lookup"><span data-stu-id="a4ba6-113">Package upgrade improvements and pending tasks</span></span>

<span data-ttu-id="a4ba6-114">Dans App-V 5.0 SP2, vous n’êtes plus invité à fermer une application virtuelle en cours d’exécution quand une nouvelle version du package ou du groupe de connexions est publiée.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-114">In App-V 5.0SP2, you are no longer prompted to close a running virtual application when a newer version of the package or connection group is published.</span></span> <span data-ttu-id="a4ba6-115">S’il s’agit d’un package ou d’un groupe de connexion utilisé lorsque vous essayez d’effectuer une tâche associée, un message s’affiche pour indiquer que l’objet est en cours d’utilisation et que l’opération sera tentée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-115">If a package or connection group is in use when you try to perform a related task, a message displays to indicate that the object is in use, and that the operation will be attempted at a later time.</span></span>

<span data-ttu-id="a4ba6-116">Les tâches qui ont été placées dans un état d’attente seront exécutées conformément aux règles suivantes:</span><span class="sxs-lookup"><span data-stu-id="a4ba6-116">Tasks that have been placed in a pending state will be performed according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a4ba6-117">Type de tâche</span><span class="sxs-lookup"><span data-stu-id="a4ba6-117">Task type</span></span></th>
<th align="left"><span data-ttu-id="a4ba6-118">Règle applicable</span><span class="sxs-lookup"><span data-stu-id="a4ba6-118">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a4ba6-119">Tâche basée sur l’utilisateur (par exemple, publication d’un package pour un utilisateur);</span><span class="sxs-lookup"><span data-stu-id="a4ba6-119">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4ba6-120">La tâche en attente sera exécutée après que l’utilisateur se déconnecte, puis se reconnecte.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-120">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a4ba6-121">Une tâche basée sur le monde (par exemple, l’activation globale d’un groupe de connexions);</span><span class="sxs-lookup"><span data-stu-id="a4ba6-121">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4ba6-122">La tâche en attente sera effectuée lorsque l’ordinateur sera arrêté, puis redémarré.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-122">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a4ba6-123">Lorsqu’une tâche est placée dans un état d’attente, le client App-V génère également une clé de Registre pour la tâche en attente, comme suit:</span><span class="sxs-lookup"><span data-stu-id="a4ba6-123">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a4ba6-124">Tâche basée sur le niveau utilisateur ou global</span><span class="sxs-lookup"><span data-stu-id="a4ba6-124">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="a4ba6-125">Emplacement de génération de la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="a4ba6-125">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a4ba6-126">Tâches basées sur l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a4ba6-126">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4ba6-127">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="a4ba6-127">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a4ba6-128">Tâches globalement basées</span><span class="sxs-lookup"><span data-stu-id="a4ba6-128">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4ba6-129">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="a4ba6-129">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a4ba6-130">Virtualisation de Microsoft Office 2013 et Microsoft Office 2010 à l’aide de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a4ba6-130">Virtualizing Microsoft Office 2013 and Microsoft Office 2010 using App-V 5.0</span></span>

<span data-ttu-id="a4ba6-131">Utilisez le lien suivant pour plus d’informations sur les scénarios Microsoft Office pris en charge par App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-131">Use the following link for more information about App-V 5.0 supported Microsoft Office scenarios.</span></span>

[<span data-ttu-id="a4ba6-132">Virtualisation de MicrosoftOffice2013 pour Application Virtualization (App-V)5.0</span><span class="sxs-lookup"><span data-stu-id="a4ba6-132">Virtualizing Microsoft Office 2013 for Application Virtualization (App-V) 5.0</span></span>](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

<span data-ttu-id="a4ba6-133">**Remarques**  Ce document porte sur la création d’un package Microsoft Office 2013 App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-133">**Note** This document focuses on creating a Microsoft Office 2013 App-V 5.0 Package.</span></span> <span data-ttu-id="a4ba6-134">Toutefois, elle fournit également des informations sur les scénarios pour Microsoft Office 2010 avec App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-134">However, it also provides information about scenarios for Microsoft Office 2010 with App-V 5.0.</span></span>

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> <span data-ttu-id="a4ba6-135">Application d’interface utilisateur de gestion des clients App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a4ba6-135">App-V 5.0 Client Management User Interface Application</span></span>

<span data-ttu-id="a4ba6-136">Dans les versions précédentes de App-V 5,0, l’interface utilisateur de gestion des clients a été fournie avec l’installation du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-136">In previous versions of App-V 5.0 the Client Management User Interface (UI) was provided with the App-V 5.0 Client installation.</span></span> <span data-ttu-id="a4ba6-137">Ce n’est plus le cas avec l’App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-137">With App-V 5.0SP2 this is no longer the case.</span></span> <span data-ttu-id="a4ba6-138">Les administrateurs ont désormais la possibilité de déployer l’interface utilisateur du client App-V 5,0 en tant qu’application virtuelle (à l’aide des configurations de déploiement App-V prises en charge) ou d’une application installée.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-138">Administrators now have the option to deploy the App-V 5.0 Client UI as a Virtual Application (using all supported App-V deployment configurations) or as an installed application.</span></span>

<span data-ttu-id="a4ba6-139">Pour plus d’informations, voir [application de l’interface utilisateur du client Microsoft application virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .</span><span class="sxs-lookup"><span data-stu-id="a4ba6-139">For more information see [Microsoft Application Virtualization 5.0 Client UI Application](https://go.microsoft.com/fwlink/p/?LinkId=386345) (https://go.microsoft.com/fwlink/?LinkId=386345).</span></span>

### <span data-ttu-id="a4ba6-140">Déploiement et déploiement automatique d’assemblys côte à côte (SxS)</span><span class="sxs-lookup"><span data-stu-id="a4ba6-140">Side-by-Side (SxS) Assembly Automatic Packaging and Deployment</span></span>

<span data-ttu-id="a4ba6-141">App-V 5.0 SP2 détecte automatiquement les assemblys côte à côte (SxS) et le déploiement sur l’ordinateur exécutant le client App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-141">App-V 5.0SP2 now automatically detects side-by-side (SxS) assemblies, and deployment on the computer running the App-V 5.0SP2 client.</span></span> <span data-ttu-id="a4ba6-142">Un assemblage SxS se compose essentiellement des dépendances du runtime VC + + ou de MSXML.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-142">A SxS assembly primarily consists of VC++ run-time dependencies or MSXML.</span></span> <span data-ttu-id="a4ba6-143">Dans les versions précédentes d’App-V, les applications virtuelles qui disposaient de dépendances sur l’exécution de VC nécessitent ces dépendances pour être effectuées localement sur l’ordinateur exécutant le client App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-143">In previous versions of App-V, virtual applications that had dependencies on VC run-times required these dependencies to be locally on the computer running the App-V 5.0SP2 client.</span></span>

<span data-ttu-id="a4ba6-144">Les fonctionnalités suivantes sont désormais prises en charge:</span><span class="sxs-lookup"><span data-stu-id="a4ba6-144">The following functionality is now supported:</span></span>

-   <span data-ttu-id="a4ba6-145">Le Sequencer App-V 5,0 capture automatiquement l’assembly SxS dans le package, que l’exécution du VC soit déjà installée sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-145">The App-V 5.0 sequencer automatically captures the SxS assembly in the package regardless of whether the VC run-time has already been installed on the computer running the sequencer.</span></span>

-   <span data-ttu-id="a4ba6-146">Le client App-V 5,0 installe automatiquement l’assembly SxS requis vers l’ordinateur exécutant le client selon les besoins au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-146">The App-V 5.0 client automatically installs the required SxS assembly to the computer running the client as required at publishing time.</span></span>

-   <span data-ttu-id="a4ba6-147">Le Sequencer App-V 5,0 signale la dépendance au moment de l’exécution VC à l’aide du mécanisme de création de rapports de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-147">The App-V 5.0 sequencer reports the VC run-time dependency using the sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="a4ba6-148">Le Sequencer App-V 5,0 vous permet désormais d’exclure la dépendance au moment de l’exécution VC dans l’éventualité où la dépendance est déjà disponible sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-148">The App-V 5.0 sequencer now allows you to exclude the VC run-time dependency in the event that the dependency is already available on the computer running the sequencer.</span></span>

### <span data-ttu-id="a4ba6-149">Améliorations de l’actualisation de la publication</span><span class="sxs-lookup"><span data-stu-id="a4ba6-149">Publishing Refresh Improvements</span></span>

<span data-ttu-id="a4ba6-150">App-V 5,0 prend en charge plusieurs fonctionnalités qui ont été ajoutées pour améliorer l’utilisation globale de l’actualisation d’un ensemble d’applications pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-150">App-V 5.0 supports several features were added to improve the overall experience of refreshing a set of applications for a specific user.</span></span>

<span data-ttu-id="a4ba6-151">La liste suivante présente les améliorations de l’actualisation de publication:</span><span class="sxs-lookup"><span data-stu-id="a4ba6-151">The following list displays the publishing refresh enhancements:</span></span>

<span data-ttu-id="a4ba6-152">La liste suivante contient des informations supplémentaires sur l’activation des nouvelles améliorations de l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-152">The following list contains more information about how to enable the new publishing refresh improvements.</span></span>

-   <span data-ttu-id="a4ba6-153">**EnablePublishingRefreshUI** : permet d’activer la barre de progression de l’actualisation de la publication pour l’ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-153">**EnablePublishingRefreshUI** - Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span>

-   <span data-ttu-id="a4ba6-154">**HideUI** -masque la barre de progression de l’actualisation de la publication lors d’une synchronisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-154">**HideUI** - Hides the publishing refresh progress bar during a manual sync.</span></span>

### <span data-ttu-id="a4ba6-155">Paramètre de configuration du nouveau client</span><span class="sxs-lookup"><span data-stu-id="a4ba6-155">New Client Configuration Setting</span></span>

<span data-ttu-id="a4ba6-156">Le paramètre de configuration de client suivant est disponible avec App-V 5,0 SP2:</span><span class="sxs-lookup"><span data-stu-id="a4ba6-156">The following new client configuration setting is available with App-V 5.0 SP2:</span></span>

<span data-ttu-id="a4ba6-157">**EnableDynamicVirtualization** -permet d’utiliser les extensions d’interpréteur de navigateur, les objets d’assistance du navigateur et les contrôles Active X pour être virtualisé et exécuté avec des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-157">**EnableDynamicVirtualization** - Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span>

<span data-ttu-id="a4ba6-158">Pour plus d’informations, voir [à propos des paramètres de configuration du client](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a4ba6-158">For more information, see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span>

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> <span data-ttu-id="a4ba6-159">Extensions d’environnement App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a4ba6-159">App-V 5.0 Shell extensions</span></span>

<span data-ttu-id="a4ba6-160">App-V 5,0 SP2 prend désormais en charge les extensions d’environnement.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-160">App-V 5.0 SP2 now supports shell extensions.</span></span>

<span data-ttu-id="a4ba6-161">Pour plus d’informations, reportez-vous à la section **prise en charge** de la [création et de la gestion des Applications virtuelles 5,0 App](creating-and-managing-app-v-50-virtualized-applications.md)-v 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-161">For more information see the **App-V 5.0SP2 shell extension support** section of [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

## <a href="" id="---------app-v-5-0-documentation-updates"></a> <span data-ttu-id="a4ba6-162">Mises à jour de la documentation App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a4ba6-162">App-V 5.0 documentation updates</span></span>


<span data-ttu-id="a4ba6-163">App-V 5,0 SP2 fournit une documentation mise à jour pour les scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="a4ba6-163">App-V 5.0 SP2 provides updated documentation for the following scenarios:</span></span>

-   [<span data-ttu-id="a4ba6-164">Migration à partir d'une version précédente</span><span class="sxs-lookup"><span data-stu-id="a4ba6-164">Migrating from a Previous Version</span></span>](migrating-from-a-previous-version-app-v-50.md)

-   [<span data-ttu-id="a4ba6-165">À propos d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="a4ba6-165">About App-V 5.0</span></span>](about-app-v-50.md)

-   <span data-ttu-id="a4ba6-166">[À propos de la création de rapports App-V 5,0](about-app-v-50-reporting.md) (section Forum aux questions)</span><span class="sxs-lookup"><span data-stu-id="a4ba6-166">[About App-V 5.0 Reporting](about-app-v-50-reporting.md) (frequently asked questions section)</span></span>

## <span data-ttu-id="a4ba6-167">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="a4ba6-167">How to Get MDOP Technologies</span></span>


<span data-ttu-id="a4ba6-168">App-V 5,0 fait partie du pack d’optimisation du bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="a4ba6-168">App-V 5.0 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="a4ba6-169">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="a4ba6-169">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="a4ba6-170">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="a4ba6-170">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="a4ba6-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4ba6-171">Related topics</span></span>


[<span data-ttu-id="a4ba6-172">Notes de publication pour App-V5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="a4ba6-172">Release Notes for App-V 5.0 SP2</span></span>](release-notes-for-app-v-50-sp2.md)

 

 





