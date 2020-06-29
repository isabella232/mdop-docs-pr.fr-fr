---
title: Vue d'ensemble des outils dans DaRT10
description: Vue d'ensemble des outils dans DaRT10
author: dansimp
ms.assetid: 752467dd-b646-4335-82ce-9090d4651f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8bef2b92e998bebffae526d4288c76be081fe0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809689"
---
# <span data-ttu-id="af145-103">Vue d'ensemble des outils dans DaRT10</span><span class="sxs-lookup"><span data-stu-id="af145-103">Overview of the Tools in DaRT 10</span></span>


<span data-ttu-id="af145-104">Depuis la fenêtre du jeu d’outils de **Diagnostics et de récupération** de Microsoft Diagnostics and Recovery Tools (DART) 10, vous pouvez démarrer l’un des outils que vous avez inclus lors de la création de l’image de récupération DART 10.</span><span class="sxs-lookup"><span data-stu-id="af145-104">From the **Diagnostics and Recovery Toolset** window in Microsoft Diagnostics and Recovery Toolset (DaRT) 10, you can start any of the individual tools that you include when you create the DaRT 10 recovery image.</span></span> <span data-ttu-id="af145-105">Pour plus d’informations sur la façon d’accéder à la fenêtre de **Diagnostics et** de l’ensemble d’outils de récupération, voir [Comment récupérer des ordinateurs locaux à l’aide de l’image de récupération DART](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="af145-105">For information about how to access the **Diagnostics and Recovery Toolset** window, see [How to Recover Local Computers by Using the DaRT Recovery Image](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md).</span></span>

<span data-ttu-id="af145-106">S’il est disponible, vous pouvez utiliser l' **Assistant solution** dans la fenêtre du **jeu d’outils de diagnostics et de récupération** pour sélectionner l’outil qui répond le mieux à votre problème spécifique, en fonction d’un bref entretien fourni par l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="af145-106">If it is available, you can use the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to select the tool that best addresses your particular issue, based on a brief interview that the wizard provides.</span></span>

## <span data-ttu-id="af145-107">Découvrir les outils DaRT</span><span class="sxs-lookup"><span data-stu-id="af145-107">Exploring the DaRT tools</span></span>


<span data-ttu-id="af145-108">La description des outils DaRT 10 suit.</span><span class="sxs-lookup"><span data-stu-id="af145-108">A description of the DaRT 10 tools follows.</span></span>

### <span data-ttu-id="af145-109">Gestion de l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="af145-109">Computer Management</span></span>

<span data-ttu-id="af145-110">**Gestion** de l’ordinateur est un ensemble d’outils d’administration Windows qui vous aident à résoudre les problèmes liés à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="af145-110">**Computer Management** is a collection of Windows administrative tools that help you troubleshoot a problem computer.</span></span> <span data-ttu-id="af145-111">Vous pouvez utiliser les outils de **gestion d’ordinateur** dans DART pour afficher des informations système et des journaux des événements, gérer des disques, afficher des Autoruns et gérer les services et pilotes.</span><span class="sxs-lookup"><span data-stu-id="af145-111">You can use the **Computer Management** tools in DaRT to view system information and event logs, manage disks, list autoruns, and manage services and drivers.</span></span> <span data-ttu-id="af145-112">La console de **gestion des ordinateurs** est personnalisée pour vous aider à diagnostiquer et réparer les problèmes susceptibles d’empêcher le démarrage du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="af145-112">The **Computer Management** console is customized to help you diagnose and repair problems that might be preventing the Windows operating system from starting.</span></span>

<span data-ttu-id="af145-113">**Remarques**  La récupération des disques dynamiques avec DaRT n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="af145-113">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="af145-114">Analyse Crash</span><span class="sxs-lookup"><span data-stu-id="af145-114">Crash Analyzer</span></span>

<span data-ttu-id="af145-115">Utilisez l' **Assistant analyse crash** pour déterminer rapidement la cause d’une panne d’ordinateur en analysant le fichier d’image mémoire sur le système d’exploitation Windows que vous réparez.</span><span class="sxs-lookup"><span data-stu-id="af145-115">Use the **Crash Analyzer Wizard** to quickly determine the cause of a computer failure by analyzing the memory dump file on the Windows operating system that you are repairing.</span></span> <span data-ttu-id="af145-116">**Crash Analyzer** examine le fichier d’image mémoire pour le pilote qui a entraîné l’échec de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="af145-116">**Crash Analyzer** examines the memory dump file for the driver that caused a computer to fail.</span></span> <span data-ttu-id="af145-117">Vous pouvez ensuite désactiver le pilote de périphérique à l’aide du nœud **services et pilotes** dans l’outil de **gestion des ordinateurs** .</span><span class="sxs-lookup"><span data-stu-id="af145-117">You can then disable the problem device driver by using the **Services and Drivers** node in the **Computer Management** tool.</span></span>

<span data-ttu-id="af145-118">L' **Assistant analyse de blocage** nécessite les outils de débogage pour Windows et les fichiers de symboles pour le système d’exploitation que vous réparez.</span><span class="sxs-lookup"><span data-stu-id="af145-118">The **Crash Analyzer Wizard** requires the Debugging Tools for Windows and symbol files for the operating system that you are repairing.</span></span> <span data-ttu-id="af145-119">Vous pouvez inclure les deux conditions requises lors de la création de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="af145-119">You can include both requirements when you create the DaRT recovery image.</span></span> <span data-ttu-id="af145-120">S’ils ne sont pas inclus dans l’image de récupération et que vous ne disposez pas de l’accès sur l’ordinateur sur lequel vous réparez, vous pouvez copier le fichier de vidage de mémoire sur un autre ordinateur et utiliser la version autonome d' **crash Analyzer** pour diagnostiquer le problème.</span><span class="sxs-lookup"><span data-stu-id="af145-120">If they are not included on the recovery image and you do not have access to them on the computer that you are repairing, you can copy the memory dump file to another computer and use the stand-alone version of **Crash Analyzer** to diagnose the problem.</span></span>

<span data-ttu-id="af145-121">L’exécution de l' **Analyseur de blocage** est une bonne idée même si vous envisagez de réorganiser votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="af145-121">Running **Crash Analyzer** is a good idea even if you plan to reimage the computer.</span></span> <span data-ttu-id="af145-122">L’image peut présenter un pilote défectueux qui pose problème dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="af145-122">The image could have a defective driver that is causing problems in your environment.</span></span> <span data-ttu-id="af145-123">L’exécution de l' **Analyseur de blocage**vous permet d’identifier les pilotes de problèmes et d’améliorer la stabilité de l’image.</span><span class="sxs-lookup"><span data-stu-id="af145-123">By running **Crash Analyzer**, you can identify problem drivers and improve the image stability.</span></span>

<span data-ttu-id="af145-124">Pour plus d’informations sur l' **analyseur d’incidents**, voir [diagnostic des pannes système avec l’analyseur d’incidents](diagnosing-system-failures-with-crash-analyzer-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="af145-124">For more information about **Crash Analyzer**, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md).</span></span>

### <span data-ttu-id="af145-125">Disk commander</span><span class="sxs-lookup"><span data-stu-id="af145-125">Disk Commander</span></span>

<span data-ttu-id="af145-126">**Disk commander** vous permet de récupérer et réparer des partitions ou volumes de disque à l’aide de l’un des processus de récupération suivants:</span><span class="sxs-lookup"><span data-stu-id="af145-126">**Disk Commander** lets you recover and repair disk partitions or volumes by using one of the following recovery processes:</span></span>

-   <span data-ttu-id="af145-127">Restaurez l’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="af145-127">Restore the master boot record (MBR)</span></span>

-   <span data-ttu-id="af145-128">Restaurer un ou plusieurs volumes perdus</span><span class="sxs-lookup"><span data-stu-id="af145-128">Recover one or more lost volumes</span></span>

-   <span data-ttu-id="af145-129">Restauration de tables de partitions à partir de **Disk commander** Backup</span><span class="sxs-lookup"><span data-stu-id="af145-129">Restore partition tables from **Disk Commander** backup</span></span>

-   <span data-ttu-id="af145-130">Enregistrer les tables de partitions dans la sauvegarde de **Disk commander**</span><span class="sxs-lookup"><span data-stu-id="af145-130">Save partition tables to **Disk Commander** backup</span></span>

<span data-ttu-id="af145-131">**Avertissement**  Nous vous recommandons de sauvegarder un disque avant d’utiliser **Disk commander** pour le réparer.</span><span class="sxs-lookup"><span data-stu-id="af145-131">**Warning** We recommend that you back up a disk before you use **Disk Commander** to repair it.</span></span> <span data-ttu-id="af145-132">En utilisant **Disk commander**, vous pouvez endommager des volumes et les rendre inaccessibles.</span><span class="sxs-lookup"><span data-stu-id="af145-132">By using **Disk Commander**, you can potentially damage volumes and make them inaccessible.</span></span> <span data-ttu-id="af145-133">De plus, les modifications apportées à un volume peuvent affecter d’autres volumes, car les volumes sur un disque partagent une table de partitions.</span><span class="sxs-lookup"><span data-stu-id="af145-133">Additionally, changes to one volume can affect other volumes because volumes on a disk share a partition table.</span></span>

 

<span data-ttu-id="af145-134">**Remarques**  La récupération des disques dynamiques avec DaRT n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="af145-134">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="af145-135">Effacement de disque</span><span class="sxs-lookup"><span data-stu-id="af145-135">Disk Wipe</span></span>

<span data-ttu-id="af145-136">Vous pouvez utiliser la **réinitialisation du disque** pour supprimer l’ensemble des données d’un disque ou d’un volume, même celles qui sont laissées après le reformatage d’un disque dur.</span><span class="sxs-lookup"><span data-stu-id="af145-136">You can use **Disk Wipe** to delete all data from a disk or volume, even the data that is left behind after you reformat a hard disk drive.</span></span> <span data-ttu-id="af145-137">L' **effacement de disque** vous permet d’effectuer une sélection à partir d’un remplacement à une seule passe ou d’une remplacement à quatre passes qui répond aux normes actuelles du ministère de la défense des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="af145-137">**Disk Wipe** lets you select from either a single-pass overwrite or a four-pass overwrite, which meets current U.S. Department of Defense standards.</span></span>

<span data-ttu-id="af145-138">**Avertissement**  Après avoir essuyé un disque ou un volume, vous ne pouvez pas récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="af145-138">**Warning** After wiping a disk or volume, you cannot recover the data.</span></span> <span data-ttu-id="af145-139">Vérifiez la taille et l’étiquette d’un volume avant de l’effacer.</span><span class="sxs-lookup"><span data-stu-id="af145-139">Verify the size and label of a volume before erasing it.</span></span>

 

### <span data-ttu-id="af145-140">Architecture</span><span class="sxs-lookup"><span data-stu-id="af145-140">Explorer</span></span>

<span data-ttu-id="af145-141">L’outil **Explorateur** vous permet de parcourir le système de fichiers et les partages réseau de l’ordinateur afin de supprimer les données importantes stockées sur le disque dur local avant d’essayer de réparer ou de réutiliser l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="af145-141">The **Explorer** tool lets you browse the computer’s file system and network shares so that you can remove important data that the user stored on the local drive before you try to repair or reimage the computer.</span></span> <span data-ttu-id="af145-142">Dans la mesure où vous pouvez mapper des lettres de lecteur aux partages réseau, vous pouvez facilement copier et déplacer des fichiers de l’ordinateur vers le réseau pour être sûr ou du réseau à l’ordinateur pour les restaurer.</span><span class="sxs-lookup"><span data-stu-id="af145-142">And because you can map drive letters to network shares, you can easily copy and move files from the computer to the network for safekeeping or from the network to the computer to restore them.</span></span>

### <span data-ttu-id="af145-143">Restauration de fichiers</span><span class="sxs-lookup"><span data-stu-id="af145-143">File Restore</span></span>

<span data-ttu-id="af145-144">La **restauration de fichiers** vous permet d’essayer de restaurer des fichiers accidentellement supprimés ou trop volumineux pour être contenus dans la corbeille.</span><span class="sxs-lookup"><span data-stu-id="af145-144">**File Restore** lets you try to restore files that were accidentally deleted or that were too big to fit in the Recycle Bin.</span></span> <span data-ttu-id="af145-145">La **restauration de fichiers** n’est pas limitée aux volumes de disque normaux, mais elle permet de rechercher et de restaurer des fichiers sur des volumes perdus ou sur des volumes chiffrés par BitLocker.</span><span class="sxs-lookup"><span data-stu-id="af145-145">**File Restore** is not limited to regular disk volumes, but can find and restore files on lost volumes or on volumes that are encrypted by BitLocker.</span></span>

<span data-ttu-id="af145-146">**Remarques**  La récupération des disques dynamiques avec DaRT n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="af145-146">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="af145-147">Recherche de fichiers</span><span class="sxs-lookup"><span data-stu-id="af145-147">File Search</span></span>

<span data-ttu-id="af145-148">Avant de répartir sur un ordinateur, il est important de récupérer des fichiers à partir du disque dur local, en particulier lorsque l’utilisateur n’a pas pu sauvegarder ou stocké les fichiers ailleurs.</span><span class="sxs-lookup"><span data-stu-id="af145-148">Before reimaging a computer, recovering files from the local hard disk is important, especially when the user might not have backed up or stored the files elsewhere.</span></span>

<span data-ttu-id="af145-149">L’outil de **recherche** permet d’ouvrir une fenêtre de **recherche de fichiers** que vous pouvez utiliser pour rechercher des documents lorsque vous ne connaissez pas le chemin d’accès du fichier ou pour rechercher des types de fichiers généraux sur tous les disques durs locaux.</span><span class="sxs-lookup"><span data-stu-id="af145-149">The **Search** tool opens a **File Search** window that you can use to find documents when you do not know the file path or to search for general kinds of files across all local hard disks.</span></span> <span data-ttu-id="af145-150">Vous pouvez rechercher des modèles de nom de fichier spécifiques dans des chemins d’accès spécifiques.</span><span class="sxs-lookup"><span data-stu-id="af145-150">You can search for specific file-name patterns in specific paths.</span></span> <span data-ttu-id="af145-151">Vous pouvez également limiter les résultats à une plage de dates ou une plage de tailles.</span><span class="sxs-lookup"><span data-stu-id="af145-151">You can also limit results to a date range or size range.</span></span>

### <span data-ttu-id="af145-152">Désinstallation de HotFix</span><span class="sxs-lookup"><span data-stu-id="af145-152">Hotfix Uninstall</span></span>

<span data-ttu-id="af145-153">L' **Assistant de désinstallation de correctif** vous permet de supprimer les correctifs ou les service packs du système d’exploitation Windows sur l’ordinateur que vous réparez.</span><span class="sxs-lookup"><span data-stu-id="af145-153">The **Hotfix Uninstall Wizard** lets you remove hotfixes or service packs from the Windows operating system on the computer that you are repairing.</span></span> <span data-ttu-id="af145-154">Utilisez cet outil lorsqu’un correctif ou un service pack est suspecté d’empêcher le démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="af145-154">Use this tool when a hotfix or service pack is suspected in preventing the operating system from starting.</span></span>

<span data-ttu-id="af145-155">Nous vous recommandons de désinstaller un seul correctif à la fois, même si cet outil vous permet d’en désinstaller plusieurs.</span><span class="sxs-lookup"><span data-stu-id="af145-155">We recommend that you uninstall only one hotfix at a time, even though the tool lets you uninstall more than one.</span></span>

<span data-ttu-id="af145-156">**Important**  Les programmes installés ou mis à jour après l’installation d’un correctif risquent de ne pas fonctionner correctement après la désinstallation d’un correctif.</span><span class="sxs-lookup"><span data-stu-id="af145-156">**Important** Programs that were installed or updated after a hotfix was installed might not work correctly after you uninstall a hotfix.</span></span>

 

### <span data-ttu-id="af145-157">Locksmith</span><span class="sxs-lookup"><span data-stu-id="af145-157">Locksmith</span></span>

<span data-ttu-id="af145-158">L' **Assistant Locksmith** vous permet de définir ou de modifier le mot de passe d’un compte local du système d’exploitation Windows que vous analysez ou réparez.</span><span class="sxs-lookup"><span data-stu-id="af145-158">The **Locksmith Wizard** lets you set or change the password for any local account on the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="af145-159">Il n’est pas nécessaire de connaître le mot de passe actuel.</span><span class="sxs-lookup"><span data-stu-id="af145-159">You do not have to know the current password.</span></span> <span data-ttu-id="af145-160">Toutefois, le mot de passe que vous définissez doit être conforme aux exigences définies par un objet de stratégie de groupe local.</span><span class="sxs-lookup"><span data-stu-id="af145-160">However, the password that you set must comply with any requirements that are defined by a local Group Policy Object.</span></span> <span data-ttu-id="af145-161">Cela inclut la longueur et la complexité des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="af145-161">This includes password length and complexity.</span></span>

<span data-ttu-id="af145-162">Vous pouvez utiliser **Locksmith** quand le mot de passe d’un compte local, tel que le compte d’administrateur local, n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="af145-162">You can use **Locksmith** when the password for a local account, such as the local Administrator account, is unknown.</span></span> <span data-ttu-id="af145-163">Vous ne pouvez pas utiliser **Locksmith** pour définir des mots de passe pour les comptes de domaine.</span><span class="sxs-lookup"><span data-stu-id="af145-163">You cannot use **Locksmith** to set passwords for domain accounts.</span></span>

### <span data-ttu-id="af145-164">Éditeur du Registre</span><span class="sxs-lookup"><span data-stu-id="af145-164">Registry Editor</span></span>

<span data-ttu-id="af145-165">Vous pouvez utiliser l' **éditeur du Registre** pour accéder à la clé de Registre du système d’exploitation Windows que vous analysez ou que vous réparez et modifier celle-ci.</span><span class="sxs-lookup"><span data-stu-id="af145-165">You can use **Registry Editor** to access and change the registry of the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="af145-166">Il s’agit de l’ajout, de la suppression et de la modification de clés et de valeurs, et de l’importation de fichiers de Registre (. reg).</span><span class="sxs-lookup"><span data-stu-id="af145-166">This includes adding, removing, and editing keys and values, and importing registry (.reg) files.</span></span>

<span data-ttu-id="af145-167">**Avertissement**  Des problèmes sérieux peuvent se produire si vous modifiez incorrectement le registre à l’aide de l' **éditeur du Registre**.</span><span class="sxs-lookup"><span data-stu-id="af145-167">**Warning** Serious problems can occur if you change the registry incorrectly by using **Registry Editor**.</span></span> <span data-ttu-id="af145-168">Ces problèmes peuvent nécessiter la réinstallation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="af145-168">These problems might require you to reinstall the operating system.</span></span> <span data-ttu-id="af145-169">Avant d’apporter des modifications au registre, il est recommandé de sauvegarder toutes les données importantes de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="af145-169">Before you make changes to the registry, you should back up any valued data on the computer.</span></span> <span data-ttu-id="af145-170">Changez de Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="af145-170">Change the registry at your own risk.</span></span>

 

### <span data-ttu-id="af145-171">Analyse SFC</span><span class="sxs-lookup"><span data-stu-id="af145-171">SFC Scan</span></span>

<span data-ttu-id="af145-172">L’outil d' **analyse SFC** démarre l' **Assistant réparation de fichiers système** et vous permet de réparer les fichiers système qui empêchent le démarrage du système d’exploitation Windows installé.</span><span class="sxs-lookup"><span data-stu-id="af145-172">The **SFC Scan** tool starts the **System File Repair Wizard** and lets you repair system files that are preventing the installed Windows operating system from starting.</span></span> <span data-ttu-id="af145-173">L' **Assistant réparation de fichier système** peut réparer automatiquement les fichiers système endommagés ou manquants, ou vous demander avant d’effectuer des réparations.</span><span class="sxs-lookup"><span data-stu-id="af145-173">The **System File Repair Wizard** can automatically repair system files that are corrupted or missing, or it can prompt you before it performs any repairs.</span></span>

### <span data-ttu-id="af145-174">Assistant solution</span><span class="sxs-lookup"><span data-stu-id="af145-174">Solution Wizard</span></span>

<span data-ttu-id="af145-175">L' **Assistant solution** présente une série de questions et recommande le meilleur outil pour la situation, en fonction de vos réponses.</span><span class="sxs-lookup"><span data-stu-id="af145-175">The **Solution Wizard** presents a series of questions and then recommends the best tool for the situation, based on your answers.</span></span> <span data-ttu-id="af145-176">Cet Assistant vous aide à déterminer quel outil utiliser lorsque vous ne connaissez pas les outils dans DaRT.</span><span class="sxs-lookup"><span data-stu-id="af145-176">This wizard helps you determine which tool to use when you are not familiar with the tools in DaRT.</span></span>

### <span data-ttu-id="af145-177">Configuration TCP/IP</span><span class="sxs-lookup"><span data-stu-id="af145-177">TCP/IP Config</span></span>

<span data-ttu-id="af145-178">Lorsque vous démarrez un ordinateur problématique dans DaRT, il est configuré pour obtenir automatiquement sa configuration TCP/IP (adresse IP et serveur DNS) à partir du protocole DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="af145-178">When you boot a problem computer into DaRT, it is set to automatically obtain its TCP/IP configuration (IP address and DNS server) from Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="af145-179">Si le protocole DHCP n’est pas disponible, vous pouvez configurer manuellement TCP/IP à l’aide de l’outil de **configuration TCP/IP** .</span><span class="sxs-lookup"><span data-stu-id="af145-179">If DHCP is unavailable, you can manually configure TCP/IP by using the **TCP/IP Config** tool.</span></span> <span data-ttu-id="af145-180">Commencez par sélectionner une carte réseau, puis configurez l’adresse IP et le serveur DNS pour cette carte.</span><span class="sxs-lookup"><span data-stu-id="af145-180">You first select a network adapter, and then configure the IP address and DNS server for that adapter.</span></span>

## <span data-ttu-id="af145-181">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af145-181">Related topics</span></span>


[<span data-ttu-id="af145-182">Prise en main de DaRT10</span><span class="sxs-lookup"><span data-stu-id="af145-182">Getting Started with DaRT 10</span></span>](getting-started-with-dart-10.md)

 

 





