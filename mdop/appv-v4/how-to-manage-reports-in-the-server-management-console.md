---
title: Procédure pour gérer les rapports dans Server Management Console
description: Procédure pour gérer les rapports dans Server Management Console
author: dansimp
ms.assetid: 28d99620-6339-43f6-9288-4aa958607c59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3d70734be04df380e6ce3f4ee8de126503e482e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806989"
---
# <span data-ttu-id="b5a36-103">Procédure pour gérer les rapports dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b5a36-103">How to Manage Reports in the Server Management Console</span></span>


<span data-ttu-id="b5a36-104">Pour gérer efficacement le système de virtualisation des applications, vous pouvez utiliser la console de gestion du serveur d’applications pour générer divers rapports qui fournissent des informations sur le système.</span><span class="sxs-lookup"><span data-stu-id="b5a36-104">To effectively manage the Application Virtualization System, you can use the Application Virtualization Server Management Console to generate a variety of reports that provide information about the system.</span></span> <span data-ttu-id="b5a36-105">Ces informations incluent des informations d’utilisation journalière pour une application spécifique ou pour toutes les applications, et le suivi des erreurs système.</span><span class="sxs-lookup"><span data-stu-id="b5a36-105">This information includes daily usage information for a specific application or all applications, and system error tracking.</span></span>

**<span data-ttu-id="b5a36-106">Remarque</span><span class="sxs-lookup"><span data-stu-id="b5a36-106">Note</span></span>**  
-   <span data-ttu-id="b5a36-107">Lors de l’installation, le script d’installation installe uniquement la version anglaise de Report Viewer.</span><span class="sxs-lookup"><span data-stu-id="b5a36-107">During installation, the installation script installs only the English language version of report viewer.</span></span> <span data-ttu-id="b5a36-108">Pour que la visionneuse de rapports affiche les informations correctes dans d’autres langues, il est nécessaire d’installer un module linguistique à partir de l’emplacement suivant: <https://go.microsoft.com/fwlink/?LinkId=131645> .</span><span class="sxs-lookup"><span data-stu-id="b5a36-108">For the report viewer to display the correct information in other languages, it is necessary to install a language pack from the following location: <https://go.microsoft.com/fwlink/?LinkId=131645>.</span></span>

-   <span data-ttu-id="b5a36-109">Lorsque vous ajoutez ou modifiez une application dans la console de gestion du serveur, vous devez vous assurer que les noms et les versions de l’application correspondent exactement à ceux des fichiers OSD.</span><span class="sxs-lookup"><span data-stu-id="b5a36-109">When you add or edit an application in the Server Management Console, you must make sure that the application names and versions exactly match those in the OSD files.</span></span> <span data-ttu-id="b5a36-110">La fonctionnalité de création de rapports utilise les champs de données noms et versions de l’application quand elle identifie les données d’utilisation des applications sur lesquelles rapporter.</span><span class="sxs-lookup"><span data-stu-id="b5a36-110">The reporting feature uses the application names and versions data fields when it identifies application usage data on which to report.</span></span> <span data-ttu-id="b5a36-111">Si les champs de données ne correspondent pas, les enregistrements d’utilisation seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="b5a36-111">If the data fields do not match, the usage records will be skipped.</span></span>

 

## <span data-ttu-id="b5a36-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b5a36-112">In This Section</span></span>


<a href="" id="application-virtualization-report-types"></a>[<span data-ttu-id="b5a36-113">Types de rapport Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="b5a36-113">Application Virtualization Report Types</span></span>](application-virtualization-report-types.md)  
<span data-ttu-id="b5a36-114">Contient des informations sur les types de rapports disponibles.</span><span class="sxs-lookup"><span data-stu-id="b5a36-114">Contains information about the available report types.</span></span>

<a href="" id="how-to-create-a-report"></a>[<span data-ttu-id="b5a36-115">Procédure pour créer un rapport</span><span class="sxs-lookup"><span data-stu-id="b5a36-115">How to Create a Report</span></span>](how-to-create-a-reportserver.md)  
<span data-ttu-id="b5a36-116">Fournit une procédure pas à pas de création d’un rapport.</span><span class="sxs-lookup"><span data-stu-id="b5a36-116">Provides a step-by-step process for creating a report.</span></span>

<a href="" id="how-to-run-a-report"></a>[<span data-ttu-id="b5a36-117">Procédure pour exécuter un rapport</span><span class="sxs-lookup"><span data-stu-id="b5a36-117">How to Run a Report</span></span>](how-to-run-a-reportserver.md)  
<span data-ttu-id="b5a36-118">Fournit une procédure pas à pas pour exécuter un rapport.</span><span class="sxs-lookup"><span data-stu-id="b5a36-118">Provides a step-by-step process for running a report.</span></span>

<a href="" id="how-to-print-a-report"></a>[<span data-ttu-id="b5a36-119">Procédure pour imprimer un rapport</span><span class="sxs-lookup"><span data-stu-id="b5a36-119">How to Print a Report</span></span>](how-to-print-a-reportserver.md)  
<span data-ttu-id="b5a36-120">Fournit une procédure détaillée pour l’impression d’un État.</span><span class="sxs-lookup"><span data-stu-id="b5a36-120">Provides a step-by-step process for printing a report.</span></span>

<a href="" id="how-to-export-a-report"></a>[<span data-ttu-id="b5a36-121">Procédure pour exporter un rapport</span><span class="sxs-lookup"><span data-stu-id="b5a36-121">How to Export a Report</span></span>](how-to-export-a-reportserver.md)  
<span data-ttu-id="b5a36-122">Fournit une procédure détaillée pour l’exportation d’un rapport.</span><span class="sxs-lookup"><span data-stu-id="b5a36-122">Provides a step-by-step process for exporting a report.</span></span>

<a href="" id="how-to-delete-a-report"></a>[<span data-ttu-id="b5a36-123">Procédure pour supprimer un rapport</span><span class="sxs-lookup"><span data-stu-id="b5a36-123">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)  
<span data-ttu-id="b5a36-124">Fournit une procédure détaillée de suppression d’un rapport.</span><span class="sxs-lookup"><span data-stu-id="b5a36-124">Provides a step-by-step process for deleting a report.</span></span>

## <span data-ttu-id="b5a36-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5a36-125">Related topics</span></span>


[<span data-ttu-id="b5a36-126">Rapport d'utilisation des applications</span><span class="sxs-lookup"><span data-stu-id="b5a36-126">Application Utilization Report</span></span>](application-utilization-reportserver.md)

[<span data-ttu-id="b5a36-127">Procédure pour effectuer des tâches d'administration dans Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="b5a36-127">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="b5a36-128">Rapport d'audit du logiciel</span><span class="sxs-lookup"><span data-stu-id="b5a36-128">Software Audit Report</span></span>](software-audit-reportserver.md)

[<span data-ttu-id="b5a36-129">Rapport d'erreurs système</span><span class="sxs-lookup"><span data-stu-id="b5a36-129">System Error Report</span></span>](system-error-reportserver.md)

[<span data-ttu-id="b5a36-130">Rapport d'utilisation du système</span><span class="sxs-lookup"><span data-stu-id="b5a36-130">System Utilization Report</span></span>](system-utilization-reportserver.md)

 

 





