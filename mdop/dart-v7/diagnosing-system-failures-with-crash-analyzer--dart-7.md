---
title: Diagnostic d'échecs du système avec l'Analyseur d'incident
description: Diagnostic d'échecs du système avec l'Analyseur d'incident
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809972"
---
# <span data-ttu-id="e55bd-103">Diagnostic d'échecs du système avec l'Analyseur d'incident</span><span class="sxs-lookup"><span data-stu-id="e55bd-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="e55bd-104">L’analyseur de blocage dans Microsoft Diagnostics and Recovery Tools Tools (DaRT) 7 vous permet de déboguer un fichier de vidage sur incident sur un ordinateur exécutant Windows, puis de diagnostiquer les erreurs d’ordinateur associées.</span><span class="sxs-lookup"><span data-stu-id="e55bd-104">The Crash Analyzer in Microsoft Diagnostics and Recovery Toolset (DaRT)7 lets you debug a crash dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="e55bd-105">L’analyseur de blocage utilise les outils de débogage de Microsoft pour Windows afin d’examiner un fichier de vidage sur incident pour le pilote qui provoquait l’échec de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e55bd-105">The Crash Analyzer uses the Microsoft Debugging Tools for Windows to examine a crash dump file for the driver that caused the computer to fail.</span></span>

## <span data-ttu-id="e55bd-106">Exécuter l’analyseur d’incidents sur un ordinateur d’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="e55bd-106">Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="e55bd-107">En règle générale, vous exécutez l’analyse crash à partir de la fenêtre de l’ensemble de diagnostics et de récupération sur un ordinateur d’utilisateur final qui rencontre des problèmes.</span><span class="sxs-lookup"><span data-stu-id="e55bd-107">Typically, you run Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="e55bd-108">L’analyseur de blocage tente de rechercher les outils de débogage pour Windows sur l’ordinateur qui rencontre le problème.</span><span class="sxs-lookup"><span data-stu-id="e55bd-108">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="e55bd-109">Si la boîte de dialogue chemin d’accès au répertoire est vide, vous devez entrer l’emplacement des outils de débogage pour Windows (vous pouvez télécharger les fichiers à partir de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="e55bd-109">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="e55bd-110">Vous devez également indiquer un chemin d’accès à l’endroit où se trouvent les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="e55bd-110">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="e55bd-111">Si vous avez inclus les outils de débogage de Microsoft pour Windows et les fichiers de symboles lors de la création de l’image de récupération DaRT, ils doivent être disponibles lorsque vous exécutez l’analyseur d’incidents sur l’ordinateur qui rencontre le problème.</span><span class="sxs-lookup"><span data-stu-id="e55bd-111">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, they should be available when you run the Crash Analyzer on the problem computer.</span></span>

[<span data-ttu-id="e55bd-112">Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final</span><span class="sxs-lookup"><span data-stu-id="e55bd-112">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## <span data-ttu-id="e55bd-113">Exécution de l’analyseur d’incident en mode autonome sur un ordinateur autre qu’un ordinateur d’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="e55bd-113">Run the Crash Analyzer in stand-alone mode on a computer other than an end-user computer</span></span>


<span data-ttu-id="e55bd-114">L’analyseur de blocage tente de rechercher les outils de débogage pour Windows sur l’ordinateur qui rencontre le problème.</span><span class="sxs-lookup"><span data-stu-id="e55bd-114">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="e55bd-115">Si la boîte de dialogue chemin d’accès au répertoire est vide, vous devez entrer l’emplacement des outils de débogage pour Windows (vous pouvez télécharger les fichiers à partir de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="e55bd-115">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="e55bd-116">Vous devez également indiquer un chemin d’accès à l’endroit où se trouvent les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="e55bd-116">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="e55bd-117">Si vous n’avez pas inclus les outils de débogage de Microsoft pour Windows et les fichiers de symboles lors de la création de l’image de récupération DaRT ou si des problèmes de taille de disque ou de connectivité réseau vous empêchent de les obtenir, vous pouvez copier le fichier de vidage à partir du problème et l’analyser sur un ordinateur sur lequel est installée la version autonome d’crash Analyzer. comme l’ordinateur d’un administrateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="e55bd-117">If you did not include the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, then you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

[<span data-ttu-id="e55bd-118">Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final</span><span class="sxs-lookup"><span data-stu-id="e55bd-118">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## <span data-ttu-id="e55bd-119">S’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="e55bd-119">Ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="e55bd-120">En général, les informations de débogage sont stockées dans un fichier de symboles différent du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="e55bd-120">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="e55bd-121">Vous devez avoir accès aux informations de symbole lors du débogage d’une application qui a cessé de répondre (par exemple, si elle a été bloquée).</span><span class="sxs-lookup"><span data-stu-id="e55bd-121">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span>

<span data-ttu-id="e55bd-122">Les fichiers de symboles sont automatiquement téléchargés lors de l’exécution de l’analyseur d’incidents.</span><span class="sxs-lookup"><span data-stu-id="e55bd-122">Symbol files are automatically downloaded when you run Crash Analyzer.</span></span> <span data-ttu-id="e55bd-123">Si votre ordinateur n’est pas connecté à Internet ou si le réseau nécessite que l’ordinateur accède à un serveur proxy HTTP, les fichiers de symboles ne peuvent pas être téléchargés.</span><span class="sxs-lookup"><span data-stu-id="e55bd-123">If the computer does not have an Internet connection or the network requires the computer to access an HTTP proxy server, the symbol files cannot be downloaded.</span></span>

[<span data-ttu-id="e55bd-124">Procédure pour s'assurer que l'Analyseur d'incident puisse accéder aux fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="e55bd-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## <span data-ttu-id="e55bd-125">Autres ressources pour diagnostiquer les échecs système avec l’analyseur d’incidents</span><span class="sxs-lookup"><span data-stu-id="e55bd-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="e55bd-126">Opérations de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="e55bd-126">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





