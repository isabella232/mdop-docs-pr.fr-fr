---
title: Référence à la commande SFTTRAY
description: Référence à la commande SFTTRAY
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806273"
---
# <span data-ttu-id="edccd-103">Référence à la commande SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="edccd-103">SFTTRAY Command Reference</span></span>


<span data-ttu-id="edccd-104">L’application de barre d’état système du client Microsoft Application Virtualization (App-V), sfttray.exe, est l’élément d’interface utilisateur principal du client App-V sur lequel les utilisateurs interagiront pendant une utilisation normale.</span><span class="sxs-lookup"><span data-stu-id="edccd-104">The Microsoft Application Virtualization (App-V) Client Tray application, sfttray.exe, is the main user interface element of the App-V Client that users will interact with during normal use.</span></span> <span data-ttu-id="edccd-105">Ce programme contrôle la diffusion et le démarrage de toutes les applications virtuelles et est accessible en cliquant avec le bouton droit sur l’icône affichée dans la zone de notification pour afficher le menu des fonctions client.</span><span class="sxs-lookup"><span data-stu-id="edccd-105">This program controls the streaming and starting of all virtual applications and is accessed by right-clicking the icon displayed in the notification area to display the menu of client functions.</span></span> <span data-ttu-id="edccd-106">Ce menu permet à l’utilisateur de charger des applications, de lancer une actualisation de publication, d’annuler une demande ou de basculer le client en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="edccd-106">The menu enables the user to load applications, start a publishing refresh, cancel a request, or change the client to offline mode.</span></span> <span data-ttu-id="edccd-107">L’utilisateur peut également fermer l’application de barre des tâches du client de virtualisation des applications et toutes les applications actives en cliquant sur **quitter**.</span><span class="sxs-lookup"><span data-stu-id="edccd-107">The user can also close the Application Virtualization Client Tray application and all active applications by clicking **Exit**.</span></span>

<span data-ttu-id="edccd-108">Par défaut, l’icône s’affiche chaque fois qu’une application virtuelle est démarrée, même si vous pouvez contrôler ce comportement à l’aide de commandes SFTTRAY.</span><span class="sxs-lookup"><span data-stu-id="edccd-108">By default, the icon is displayed whenever a virtual application is started, although you can control this behavior by using SFTTRAY commands.</span></span> <span data-ttu-id="edccd-109">L’application de la barre d’état système du client de virtualisation des applications affiche également une barre de progression pour chaque application démarrée ainsi que des messages d’État sur les applications actives.</span><span class="sxs-lookup"><span data-stu-id="edccd-109">The Application Virtualization Client Tray application also displays a progress bar for each application that is started, as well as status messages about active applications.</span></span> <span data-ttu-id="edccd-110">Lorsque vous cliquez sur la barre de progression, un message s’affiche pour vous permettre d’annuler le chargement ou le démarrage d’une application.</span><span class="sxs-lookup"><span data-stu-id="edccd-110">Clicking the progress bar displays a message that allows you to cancel the loading or starting of an application.</span></span>

## <span data-ttu-id="edccd-111">Commandes SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="edccd-111">SFTTRAY Commands</span></span>


<span data-ttu-id="edccd-112">Vous pouvez afficher la liste des commandes et des commutateurs de ligne de commande en exécutant la commande suivante à partir d’une fenêtre de commande.</span><span class="sxs-lookup"><span data-stu-id="edccd-112">The list of commands and command-line switches can be displayed by running the following command from a command window.</span></span>

**<span data-ttu-id="edccd-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="edccd-113">Note</span></span>**  
<span data-ttu-id="edccd-114">Il n’y a qu’une seule instance de barre d’État du client de virtualisation d’application pour chaque contexte d’utilisateur, de sorte que si vous démarrez une nouvelle commande SFTTRAY, celle-ci sera transmise au programme déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="edccd-114">There is only one Application Virtualization Client Tray instance for each user context, so if you start a new SFTTRAY command, it will be passed to the program that is already running.</span></span>



`Sfttray.exe /?`

### <span data-ttu-id="edccd-115">Utilisation des commandes</span><span class="sxs-lookup"><span data-stu-id="edccd-115">Command Usage</span></span>

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### <span data-ttu-id="edccd-116">Commutateurs de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="edccd-116">Command-Line Switches</span></span>

<span data-ttu-id="edccd-117">Le tableau suivant décrit les commutateurs de la ligne de commande SFTTRAY.</span><span class="sxs-lookup"><span data-stu-id="edccd-117">The SFTTRAY command-line switches are described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edccd-118">Commutateur</span><span class="sxs-lookup"><span data-stu-id="edccd-118">Switch</span></span></th>
<th align="left"><span data-ttu-id="edccd-119">Description</span><span class="sxs-lookup"><span data-stu-id="edccd-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edccd-120">/HIDE</span><span class="sxs-lookup"><span data-stu-id="edccd-120">/HIDE</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-121">Masque l’icône SFTTRAY dans la zone de notification Windows.</span><span class="sxs-lookup"><span data-stu-id="edccd-121">Hides the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edccd-122">/SHOW</span><span class="sxs-lookup"><span data-stu-id="edccd-122">/SHOW</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-123">Affiche l’icône SFTTRAY dans la zone de notification Windows.</span><span class="sxs-lookup"><span data-stu-id="edccd-123">Displays the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edccd-124">/QUIET</span><span class="sxs-lookup"><span data-stu-id="edccd-124">/QUIET</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-125">Prend en charge l’utilisation sans assistance en empêchant les erreurs d’affichage des boîtes de message qui nécessitent un accusé de réception de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="edccd-125">Supports unattended usage by preventing errors from displaying message boxes that require user acknowledgement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edccd-126">/EXE &lt; -exe alternatif&gt;</span><span class="sxs-lookup"><span data-stu-id="edccd-126">/EXE &lt;alternate-exe&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-127">Utilisé avec/LAUNCH pour spécifier qu’un programme exécutable doit être démarré dans l’environnement virtuel lorsqu’une application virtuelle est démarrée à la place du fichier cible spécifié dans l’OSD.</span><span class="sxs-lookup"><span data-stu-id="edccd-127">Used with /LAUNCH to specify that an executable program is to be started in the virtual environment when a virtual application is started in place of the target file specified in the OSD.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="edccd-128">Remarque</span><span class="sxs-lookup"><span data-stu-id="edccd-128">Note</span></span></strong><br/><p><span data-ttu-id="edccd-129">Par exemple, utilisez «SFTTRAY.EXE/EXE REGEDIT.EXE &lt; application/Launch &gt; » pour examiner le registre de l’environnement virtuel dans lequel l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="edccd-129">For example, use “SFTTRAY.EXE /EXE REGEDIT.EXE /LAUNCH &lt;app&gt;” to enable you to examine the registry of the virtual environment in which the application is running.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edccd-130">&lt;Application/Launch &gt; [ &lt; args &gt; ]</span><span class="sxs-lookup"><span data-stu-id="edccd-130">/LAUNCH &lt;app&gt; [&lt;args&gt;]</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-131">Démarre une application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="edccd-131">Starts a virtual application.</span></span> <span data-ttu-id="edccd-132">Spécifiez le nom et la version d’une application ou son chemin d’accès à un fichier OSD.</span><span class="sxs-lookup"><span data-stu-id="edccd-132">Specify the name and version of an application or the path to an OSD file.</span></span> <span data-ttu-id="edccd-133">Les arguments de ligne de commande peuvent éventuellement être transmis à l’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="edccd-133">Optionally, command-line arguments can be passed to the virtual application.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="edccd-134">Remarque</span><span class="sxs-lookup"><span data-stu-id="edccd-134">Note</span></span></strong><br/><p><span data-ttu-id="edccd-135">Utilisez la commande «SFTMIME.EXE/QUERY OBJ: APP/SHORT» pour obtenir une liste des noms et versions des applications virtuelles disponibles.</span><span class="sxs-lookup"><span data-stu-id="edccd-135">Use the command “SFTMIME.EXE /QUERY OBJ:APP /SHORT” to obtain a list of the names and versions of available virtual applications.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edccd-136">/LOAD</span><span class="sxs-lookup"><span data-stu-id="edccd-136">/LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-137">Charge ou importe une application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="edccd-137">Loads or imports a virtual application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edccd-138">/LOADALL</span><span class="sxs-lookup"><span data-stu-id="edccd-138">/LOADALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-139">Charge toutes les applications dans le cache.</span><span class="sxs-lookup"><span data-stu-id="edccd-139">Loads all applications into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edccd-140">/REFRESHALL</span><span class="sxs-lookup"><span data-stu-id="edccd-140">/REFRESHALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-141">Lance une actualisation de publication pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="edccd-141">Starts a publishing refresh for all applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edccd-142">&lt;ID unique de/LAUNCHRESULT&gt;</span><span class="sxs-lookup"><span data-stu-id="edccd-142">/LAUNCHRESULT &lt;UNIQUE ID&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-143">Retourne le code de résultat de lancement du processus qui lance sfttray.exe à l’aide d’un événement global et d’un fichier mappé en mémoire qui est basé sur le nom de racine spécifié pour l’ID UNIQUE. ¹</span><span class="sxs-lookup"><span data-stu-id="edccd-143">Returns the launch result code to the process that launches sfttray.exe by using a global event and a memory mapped file that are based on the specified root name for the UNIQUE ID.¹</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edccd-144">/SFTFILE &lt; SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="edccd-144">/SFTFILE &lt;sft&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-145">Commutateur facultatif utilisé avec/LOAD pour spécifier le chemin d’accès au fichier SFT de l’application.</span><span class="sxs-lookup"><span data-stu-id="edccd-145">Optional switch used with /LOAD to specify the path to the application’s SFT file.</span></span> <span data-ttu-id="edccd-146">Si ce paramètre est spécifié, l’application est importée au lieu d’être chargée.</span><span class="sxs-lookup"><span data-stu-id="edccd-146">If specified, the application is imported rather than loaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edccd-147">/EXIT</span><span class="sxs-lookup"><span data-stu-id="edccd-147">/EXIT</span></span></p></td>
<td align="left"><p><span data-ttu-id="edccd-148">Ferme le programme SFTTRAY et toutes les applications virtuelles actives, et supprime l’icône dans la zone de notification Windows.</span><span class="sxs-lookup"><span data-stu-id="edccd-148">Closes the SFTTRAY program and all active virtual applications and removes the icon from the Windows notification area.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="edccd-149">Remarque</span><span class="sxs-lookup"><span data-stu-id="edccd-149">Note</span></span>**  
<span data-ttu-id="edccd-150">¹ le paramètre de ligne de commande */LAUNCHRESULT* fournit un moyen pour le processus qui lance sfttray.exe pour spécifier le nom racine d’un événement global et un fichier mappé en mémoire qui sont utilisés pour renvoyer le code de résultat de lancement au processus.</span><span class="sxs-lookup"><span data-stu-id="edccd-150">¹ The */LAUNCHRESULT* command line parameter provides a means for the process that launches sfttray.exe to specify the root name for a global event and a memory mapped file that are used to return the launch result code to the process.</span></span> <span data-ttu-id="edccd-151">Le nom de l’identificateur unique doit commencer par «SFT» pour empêcher la virtualisation du nom de l’événement lorsque le processus de lancement est appelé dans un environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="edccd-151">The unique identifier name should start with “SFT-” to prevent the event name from getting virtualized when the launching process is invoked within a virtual environment.</span></span> <span data-ttu-id="edccd-152">La taille de la région mappée en mémoire sera de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="edccd-152">The memory mapped region will be 64 bits in size.</span></span>

<span data-ttu-id="edccd-153">Pour utiliser ce paramètre, le processus de lancement crée un événement avec le nom « &lt; ID unique &gt; -result \ _Event», un fichier mappé en mémoire portant le nom «ID unique- &lt; result \ &gt; _Value» et éventuellement un événement portant le nom «ID &lt; unique &gt; --Shutdown \ _Event», puis le processus de lancement démarre sfttray.exe et attend que l’événement soit signalé.</span><span class="sxs-lookup"><span data-stu-id="edccd-153">To use this parameter, the launching process creates an event with the name “&lt;UNIQUE ID&gt;-result\_event”, a memory mapped file with the name “&lt;UNIQUE ID&gt;-result\_value”, and optionally an event with the name “&lt;UNIQUE ID&gt;-shutdown\_event”, and then the launching process launches sfttray.exe and waits on the event to be signaled.</span></span> <span data-ttu-id="edccd-154">Après que l’événement « &lt; ID unique &gt; -result \ _Event» est signalé, le processus de lancement récupère le code de retour de 64 bits à partir de la région mappée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="edccd-154">After the event “&lt;UNIQUE ID&gt;-result\_event” is signaled, the launching process retrieves the 64-bit return code from the memory mapped region.</span></span>

<span data-ttu-id="edccd-155">Si l’événement facultatif « &lt; ID unique &gt; -shutdown \ _Event» existe lors de la fermeture de l’application virtuelle, sfttray.exe s’ouvre et signale l’événement.</span><span class="sxs-lookup"><span data-stu-id="edccd-155">If the optional event “&lt;UNIQUE ID&gt;-shutdown\_event” exists when the virtual application exits, sfttray.exe opens and signals the event.</span></span> <span data-ttu-id="edccd-156">Le processus de lancement attend ce événement d’arrêt s’il a besoin de déterminer à quel moment l’application virtuelle s’arrête.</span><span class="sxs-lookup"><span data-stu-id="edccd-156">The launching process waits on this shutdown event if it needs to determine when the virtual application exits.</span></span>











