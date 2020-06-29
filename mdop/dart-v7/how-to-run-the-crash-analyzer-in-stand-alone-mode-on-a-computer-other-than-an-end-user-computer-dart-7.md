---
title: Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final
description: Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809564"
---
# <span data-ttu-id="41711-103">Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final</span><span class="sxs-lookup"><span data-stu-id="41711-103">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>


<span data-ttu-id="41711-104">Si vous ne parvenez pas à accéder aux outils de débogage de Microsoft pour Windows ou aux fichiers de symboles de l’ordinateur de l’utilisateur final, vous pouvez copier le fichier de vidage à partir de l’ordinateur qui rencontre un problème et l’analyser sur un ordinateur sur lequel est installée la version autonome d’crash Analyzer, telle que l’ordinateur d’un administrateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="41711-104">If you cannot access the Microsoft Debugging Tools for Windows or the symbol files on the end-user computer, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

**<span data-ttu-id="41711-105">Pour exécuter l’analyseur d’incident en mode indépendant</span><span class="sxs-lookup"><span data-stu-id="41711-105">To run the Crash Analyzer in stand-alone mode</span></span>**

1.  <span data-ttu-id="41711-106">Sur un ordinateur sur lequel DaRT7 est installé, cliquez sur **Démarrer**  /  **tous les programmes**  /  **Microsoft DART 7**.</span><span class="sxs-lookup"><span data-stu-id="41711-106">On a computer with DaRT7 installed, click **Start** / **All Programs** / **Microsoft DaRT 7**.</span></span>

2.  <span data-ttu-id="41711-107">Fournissez les informations requises pour les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="41711-107">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="41711-108">Outils de débogage de Microsoft pour Windows</span><span class="sxs-lookup"><span data-stu-id="41711-108">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="41711-109">Fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="41711-109">Symbol files</span></span>

        <span data-ttu-id="41711-110">Pour plus d’informations sur les fichiers de symboles, voir [Comment s’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="41711-110">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="41711-111">Fichier de vidage sur incident</span><span class="sxs-lookup"><span data-stu-id="41711-111">A crash dump file</span></span>

        <span data-ttu-id="41711-112">**Remarques**  Utilisez l’outil de recherche dans DaRT7 pour rechercher le fichier de vidage sur incident copié.</span><span class="sxs-lookup"><span data-stu-id="41711-112">**Note** Use the Search tool in DaRT7 to locate the copied crash dump file.</span></span>

         

3.  <span data-ttu-id="41711-113">L' **Analyseur de blocage** analyse le fichier de vidage sur incident et signale la cause probable du blocage.</span><span class="sxs-lookup"><span data-stu-id="41711-113">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="41711-114">Vous pouvez afficher des informations supplémentaires sur le blocage, comme le message d’incident et la description spécifiques, les pilotes chargés au moment du blocage et la sortie complète de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="41711-114">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="41711-115">Décidez d’une stratégie appropriée pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="41711-115">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="41711-116">Cela risque de désactiver ou de mettre à jour le pilote de périphérique à l’origine du blocage à l’aide du nœud **services et pilotes** de l’outil de gestion de l' **ordinateur** dans DART.</span><span class="sxs-lookup"><span data-stu-id="41711-116">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="41711-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41711-117">Related topics</span></span>


[<span data-ttu-id="41711-118">Diagnostic d'échecs du système avec l'Analyseur d'incident</span><span class="sxs-lookup"><span data-stu-id="41711-118">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





