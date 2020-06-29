---
title: Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final
description: Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810194"
---
# <span data-ttu-id="18b2a-103">Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final</span><span class="sxs-lookup"><span data-stu-id="18b2a-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="18b2a-104">En règle générale, vous exécutez l’analyseur de diagnostics et de récupération d’outils de diagnostics (DaRT) 7 crash Analyzer depuis la fenêtre du jeu d’outils de diagnostics et de récupération sur un ordinateur d’utilisateur final qui rencontre des problèmes.</span><span class="sxs-lookup"><span data-stu-id="18b2a-104">Typically, you run Microsoft Diagnostics and Recovery Toolset (DaRT)7 Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="18b2a-105">L’analyseur de blocage tente de rechercher les outils de débogage pour Windows sur l’ordinateur qui rencontre le problème.</span><span class="sxs-lookup"><span data-stu-id="18b2a-105">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="18b2a-106">Si la boîte de dialogue chemin d’accès au répertoire est vide, vous devez entrer l’emplacement des outils de débogage pour Windows (vous pouvez télécharger les fichiers à partir de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="18b2a-106">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="18b2a-107">Vous devez également indiquer un chemin d’accès à l’endroit où se trouvent les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="18b2a-107">You must also provide a path to where the symbol files are located.</span></span>

**<span data-ttu-id="18b2a-108">Pour ouvrir et exécuter l’analyseur d’incidents sur un ordinateur d’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="18b2a-108">To open and run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="18b2a-109">Dans la fenêtre **jeu d’outils de diagnostics et de récupération** sur un ordinateur d’utilisateur final, cliquez sur **crash Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="18b2a-109">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="18b2a-110">Fournissez les informations requises pour les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="18b2a-110">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="18b2a-111">Outils de débogage de Microsoft pour Windows</span><span class="sxs-lookup"><span data-stu-id="18b2a-111">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="18b2a-112">Fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="18b2a-112">Symbol files</span></span>

        <span data-ttu-id="18b2a-113">Pour plus d’informations sur les fichiers de symboles, voir [Comment s’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="18b2a-113">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="18b2a-114">Fichier de vidage sur incident</span><span class="sxs-lookup"><span data-stu-id="18b2a-114">A crash dump file</span></span>

        <span data-ttu-id="18b2a-115">Pour déterminer l’emplacement du fichier de vidage sur incident, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="18b2a-115">Follow these steps to determine the location of the crash dump file:</span></span>

        1.  <span data-ttu-id="18b2a-116">Ouvrez la fenêtre de **Propriétés système** .</span><span class="sxs-lookup"><span data-stu-id="18b2a-116">Open the **System Properties** window.</span></span>

            <span data-ttu-id="18b2a-117">Cliquez sur **Démarrer**, tapez sysdm.cpl, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="18b2a-117">Click **Start**, type sysdm.cpl, and then press Enter.</span></span>

        2.  <span data-ttu-id="18b2a-118">Cliquez sur l’onglet **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="18b2a-118">Click the **Advanced** tab.</span></span>

        3.  <span data-ttu-id="18b2a-119">Dans la zone **démarrage et récupération** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="18b2a-119">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="18b2a-120">**Remarques**  Si vous n’avez pas accès à la fenêtre de **Propriétés système** , vous pouvez rechercher des fichiers de vidage sur l’ordinateur de l’utilisateur final à l’aide de l’outil de **recherche** dans DART.</span><span class="sxs-lookup"><span data-stu-id="18b2a-120">**Note** If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in DaRT.</span></span>

         

3.  <span data-ttu-id="18b2a-121">L' **Analyseur de blocage** analyse le fichier de vidage sur incident et signale la cause probable du blocage.</span><span class="sxs-lookup"><span data-stu-id="18b2a-121">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="18b2a-122">Vous pouvez afficher des informations supplémentaires sur le blocage, comme le message d’incident et la description spécifiques, les pilotes chargés au moment du blocage et la sortie complète de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="18b2a-122">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="18b2a-123">Décidez d’une stratégie appropriée pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="18b2a-123">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="18b2a-124">Cela risque de désactiver ou de mettre à jour le pilote de périphérique à l’origine du blocage à l’aide du nœud **services et pilotes** de l’outil de gestion de l' **ordinateur** dans DART.</span><span class="sxs-lookup"><span data-stu-id="18b2a-124">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="18b2a-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18b2a-125">Related topics</span></span>


[<span data-ttu-id="18b2a-126">Diagnostic d'échecs du système avec l'Analyseur d'incident</span><span class="sxs-lookup"><span data-stu-id="18b2a-126">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





