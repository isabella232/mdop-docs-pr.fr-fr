---
title: Diagnostic d'échecs du système avec l'Analyseur d'incident
description: Diagnostic d'échecs du système avec l'Analyseur d'incident
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810619"
---
# <span data-ttu-id="e4417-103">Diagnostic d'échecs du système avec l'Analyseur d'incident</span><span class="sxs-lookup"><span data-stu-id="e4417-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="e4417-104">L' **Analyseur de blocage** dans Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 vous permet de déboguer un fichier de vidage de mémoire sur un ordinateur exécutant Windows, puis de diagnostiquer les erreurs d’ordinateur associées.</span><span class="sxs-lookup"><span data-stu-id="e4417-104">The **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 lets you debug a memory dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="e4417-105">L' **Analyseur de blocage** utilise les outils de débogage de Microsoft pour Windows afin d’examiner un fichier de vidage de mémoire pour le pilote ayant entraîné l’échec de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e4417-105">The **Crash Analyzer** uses the Microsoft Debugging Tools for Windows to examine a memory dump file for the driver that caused the computer to fail.</span></span> <span data-ttu-id="e4417-106">Vous pouvez exécuter l’analyseur d’incident sur un ordinateur d’utilisateur final ou en mode autonome sur un ordinateur autre qu’un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="e4417-106">You can run the Crash Analyzer on an end-user computer or in stand-alone mode on a computer other than an end-user computer.</span></span>

## <span data-ttu-id="e4417-107">Exécuter l’analyseur d’incidents sur un ordinateur d’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="e4417-107">Run the Crash Analyzer on an end-user-computer</span></span>


<span data-ttu-id="e4417-108">En règle générale, vous exécutez l' **analyse crash** à partir de la fenêtre du **jeu d’outils de diagnostics et de récupération** sur un ordinateur d’utilisateur final qui rencontre le problème.</span><span class="sxs-lookup"><span data-stu-id="e4417-108">Typically, you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing the problem.</span></span> <span data-ttu-id="e4417-109">L' **Analyseur de blocage** tente de rechercher les outils de débogage pour Windows sur l’ordinateur qui rencontre le problème.</span><span class="sxs-lookup"><span data-stu-id="e4417-109">The **Crash Analyzer** tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="e4417-110">Si la boîte de dialogue chemin d’accès au répertoire est vide, vous devez entrer l’emplacement ou accéder à l’emplacement des outils de débogage pour Windows (vous pouvez télécharger les fichiers à partir de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="e4417-110">If the directory path dialog box is empty, you must enter the location, or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="e4417-111">Vous devez également indiquer un chemin d’accès à l’endroit où se trouvent les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="e4417-111">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="e4417-112">Si vous avez inclus les outils de débogage de Microsoft pour Windows et les fichiers de symboles lors de la création de l’image de récupération 8,0 de DaRT, les outils et fichiers de symboles doivent être disponibles lorsque vous exécutez l' **analyseur d’incidents** sur l’ordinateur qui rencontre le problème.</span><span class="sxs-lookup"><span data-stu-id="e4417-112">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT 8.0 recovery image, the Tools and symbol files should be available when you run the **Crash Analyzer** on the problem computer.</span></span> <span data-ttu-id="e4417-113">Si vous ne l’avez pas inclus dans l’image de récupération DaRT, ou si les problèmes de taille de disque ou de connectivité réseau vous empêchent de les obtenir, vous pouvez également exécuter l’analyseur d’incident en mode autonome sur un ordinateur autre que l’ordinateur de l’utilisateur final, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="e4417-113">If you did not include them in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, you can alternatively run the Crash Analyzer in stand-alone mode on a computer other than the end user’s computer, as described in the following section.</span></span>

[<span data-ttu-id="e4417-114">Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final</span><span class="sxs-lookup"><span data-stu-id="e4417-114">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a><span data-ttu-id="e4417-115">Exécution de l’analyseur d’incident en mode autonome sur un ordinateur autre que l’ordinateur d’un utilisateur final</span><span class="sxs-lookup"><span data-stu-id="e4417-115">Run the Crash Analyzer in stand-alone mode on a computer other than an end user’s computer</span></span>


<span data-ttu-id="e4417-116">Même si vous exécutez généralement **crash Analyzer** sur l’ordinateur de l’utilisateur final qui rencontre le problème, vous pouvez également exécuter l’analyseur d’incident en mode autonome, sur un ordinateur autre qu’un ordinateur d’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="e4417-116">Although you typically run **Crash Analyzer** on the end-user computer that is experiencing the problem, you can also run the Crash Analyzer in stand-alone mode, on a computer other than an end-user computer.</span></span> <span data-ttu-id="e4417-117">Vous pouvez opter pour cette option si vous n’avez pas inclus les outils de débogage Windows dans l’image de récupération DaRT ou si les problèmes de taille de disque ou de connectivité réseau vous empêchent d’obtenir les outils de débogage.</span><span class="sxs-lookup"><span data-stu-id="e4417-117">You might choose this option if you did not include the Windows Debugging Tools in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining the Debugging Tools.</span></span> <span data-ttu-id="e4417-118">Dans ce cas, vous pouvez copier le fichier de vidage à partir du problème et l’analyser sur un ordinateur sur lequel est installée la version autonome d' **crash Analyzer** , par exemple sur un ordinateur de l’agent de support technique.</span><span class="sxs-lookup"><span data-stu-id="e4417-118">In this case, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of **Crash Analyzer** installed, such as on a help desk agent’s computer.</span></span>

[<span data-ttu-id="e4417-119">Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final</span><span class="sxs-lookup"><span data-stu-id="e4417-119">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## <span data-ttu-id="e4417-120">Comment s’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="e4417-120">How to ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="e4417-121">Pour déboguer des applications qui ont cessé de répondre, vous devez accéder au fichier de symboles, qui est distinct du programme.</span><span class="sxs-lookup"><span data-stu-id="e4417-121">To debug applications that have stopped responding, you need access to the symbol file, which is separate from the program.</span></span> <span data-ttu-id="e4417-122">Bien que les fichiers de symboles soient automatiquement téléchargés lors de l’exécution de l’analyseur d’incidents, il peut arriver que le problème ne soit pas possible d’accéder à Internet.</span><span class="sxs-lookup"><span data-stu-id="e4417-122">Although symbol files are automatically downloaded when you run Crash Analyzer, there might be times when the problem computer does not have access to the Internet.</span></span> <span data-ttu-id="e4417-123">Il existe plusieurs façons de vérifier que vous avez garanti l’accès aux fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="e4417-123">There are several ways to ensure that you have guaranteed access to symbol files.</span></span>

[<span data-ttu-id="e4417-124">Procédure pour s'assurer que l'Analyseur d'incident puisse accéder aux fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="e4417-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## <span data-ttu-id="e4417-125">Autres ressources pour diagnostiquer les échecs système avec l’analyseur d’incidents</span><span class="sxs-lookup"><span data-stu-id="e4417-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="e4417-126">Opérations de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="e4417-126">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





