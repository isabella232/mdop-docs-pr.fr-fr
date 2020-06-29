---
title: Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final
description: Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final
author: dansimp
ms.assetid: 10334800-ff8e-43ac-a9c2-d28807473ec2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4abf1ba2ae1a0cb1dfb129c1f5a26e11f5045290
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809492"
---
# <span data-ttu-id="49d2e-103">Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final</span><span class="sxs-lookup"><span data-stu-id="49d2e-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="49d2e-104">Pour exécuter l' **analyseur d’incidents** à partir de la fenêtre du **jeu d’outils de diagnostics et de récupération** sur un ordinateur d’utilisateur final rencontrant des problèmes, vous devez disposer des outils de débogage Microsoft pour Windows et des fichiers de symboles installés.</span><span class="sxs-lookup"><span data-stu-id="49d2e-104">To run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing problems, you must have the Microsoft Debugging Tools for Windows and the symbol files installed.</span></span> <span data-ttu-id="49d2e-105">Pour télécharger les outils de débogage Windows, voir [outils de débogage pour Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="49d2e-105">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span>

**<span data-ttu-id="49d2e-106">Pour exécuter l’analyseur d’incidents sur un ordinateur d’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="49d2e-106">To run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="49d2e-107">Dans la fenêtre **jeu d’outils de diagnostics et de récupération** sur un ordinateur d’utilisateur final, cliquez sur **crash Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="49d2e-107">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="49d2e-108">Fournissez les informations requises pour les outils de débogage de Microsoft pour Windows.</span><span class="sxs-lookup"><span data-stu-id="49d2e-108">Provide the required information for the Microsoft Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="49d2e-109">Fournissez les informations requises pour les fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="49d2e-109">Provide the required information for the symbol files.</span></span> <span data-ttu-id="49d2e-110">Pour plus d’informations sur les fichiers de symboles, voir [Comment s’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="49d2e-110">For more information about symbol files, see [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).</span></span>

4.  <span data-ttu-id="49d2e-111">Fournissez les informations requises pour un fichier de vidage de mémoire.</span><span class="sxs-lookup"><span data-stu-id="49d2e-111">Provide the required information for a memory dump file.</span></span> <span data-ttu-id="49d2e-112">Pour déterminer l’emplacement du fichier de vidage de mémoire:</span><span class="sxs-lookup"><span data-stu-id="49d2e-112">To determine the location of the memory dump file:</span></span>

    1.  <span data-ttu-id="49d2e-113">Ouvrez la fenêtre de **Propriétés système** .</span><span class="sxs-lookup"><span data-stu-id="49d2e-113">Open the **System Properties** window.</span></span>

    2.  <span data-ttu-id="49d2e-114">Cliquez sur **Démarrer**, tapez **sysdm.cpl**, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="49d2e-114">Click **Start**, type **sysdm.cpl**, and then press **Enter**.</span></span>

    3.  <span data-ttu-id="49d2e-115">Cliquez sur l’onglet **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="49d2e-115">Click the **Advanced** tab.</span></span>

    4.  <span data-ttu-id="49d2e-116">Dans la zone **démarrage et récupération** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="49d2e-116">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="49d2e-117">Si vous n’avez pas accès à la fenêtre de **Propriétés système** , vous pouvez rechercher des fichiers de vidage sur l’ordinateur de l’utilisateur final à l’aide de l’outil de **recherche** dans Microsoft Diagnostics and Recovery Tools (DART) 10.</span><span class="sxs-lookup"><span data-stu-id="49d2e-117">If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span>

    <span data-ttu-id="49d2e-118">Le **crash Analyzer** analyse le fichier de vidage de la mémoire et signale la cause probable du problème.</span><span class="sxs-lookup"><span data-stu-id="49d2e-118">The **Crash Analyzer** scans the memory dump file and reports a probable cause of the problem.</span></span> <span data-ttu-id="49d2e-119">Vous pouvez afficher des informations supplémentaires sur l’échec, par exemple le message de vidage de mémoire et la description spécifiques, les pilotes chargés au moment de l’échec et la sortie complète de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="49d2e-119">You can view more information about the failure, such as the specific memory dump message and description, the drivers loaded at the time of the failure, and the full output of the analysis.</span></span>

5.  <span data-ttu-id="49d2e-120">Identifiez la stratégie appropriée pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="49d2e-120">Identify the appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="49d2e-121">La stratégie est susceptible de nécessiter la désactivation ou la mise à jour du pilote de périphérique à l’origine de l’échec à l’aide du nœud **services et pilotes** de l’outil de gestion de l' **ordinateur** dans DART 10.</span><span class="sxs-lookup"><span data-stu-id="49d2e-121">The strategy may require disabling or updating the device driver that caused the failure by using the **Services and Drivers** node of the **Computer Management** tool in DaRT 10.</span></span>

## <span data-ttu-id="49d2e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49d2e-122">Related topics</span></span>


[<span data-ttu-id="49d2e-123">Diagnostic d'échecs du système avec l'Analyseur d'incident</span><span class="sxs-lookup"><span data-stu-id="49d2e-123">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[<span data-ttu-id="49d2e-124">Opérations de DaRT10</span><span class="sxs-lookup"><span data-stu-id="49d2e-124">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

 

 





