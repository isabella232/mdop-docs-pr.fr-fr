---
title: Rapport d'utilisation du système
description: Rapport d'utilisation du système
author: dansimp
ms.assetid: 4d490d15-2d1f-4f2c-99bb-0685447c0672
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe7ff547d969c63ace234104c3e6b7146da2c113
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806233"
---
# <span data-ttu-id="816e1-103">Rapport d'utilisation du système</span><span class="sxs-lookup"><span data-stu-id="816e1-103">System Utilization Report</span></span>


<span data-ttu-id="816e1-104">Utilisez le rapport utilisation du système pour représenter la totalité de l’utilisation du système quotidien.</span><span class="sxs-lookup"><span data-stu-id="816e1-104">Use the System Utilization Report to graph the total daily system usage.</span></span> <span data-ttu-id="816e1-105">Vous pouvez utiliser ce rapport pour déterminer la charge de votre système de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="816e1-105">You can use this report to determine the load on your Application Virtualization System.</span></span>

<span data-ttu-id="816e1-106">Ce rapport effectue le suivi de l’utilisation au cours de la période de rapport du serveur spécifié ou du groupe de serveurs.</span><span class="sxs-lookup"><span data-stu-id="816e1-106">This report tracks the usage over time during the reporting period for the specified server or for the server group.</span></span>

<span data-ttu-id="816e1-107">Le rapport sur l’utilisation du système graphique également l’utilisation système suivante:</span><span class="sxs-lookup"><span data-stu-id="816e1-107">The System Utilization Report also graphs the following system usage:</span></span>

-   <span data-ttu-id="816e1-108">Utilisation selon le jour de la semaine</span><span class="sxs-lookup"><span data-stu-id="816e1-108">Usage by day of the week</span></span>

-   <span data-ttu-id="816e1-109">Utilisation par heure du jour</span><span class="sxs-lookup"><span data-stu-id="816e1-109">Usage by hour of the day</span></span>

<span data-ttu-id="816e1-110">Le rapport sur l’utilisation du système inclut également un résumé de l’utilisation totale du système pour des utilisateurs spécifiques et du nombre total de sessions.</span><span class="sxs-lookup"><span data-stu-id="816e1-110">The System Utilization Report also includes a summary of the total system usage for specific users and total session counts.</span></span>

<span data-ttu-id="816e1-111">Lorsque vous créez un rapport, vous spécifiez les paramètres qui sont utilisés pour la collecte des données lors de l’exécution du rapport.</span><span class="sxs-lookup"><span data-stu-id="816e1-111">When you create a report, you specify the parameters that are used for collecting the data when the report is run.</span></span>

<span data-ttu-id="816e1-112">Les rapports ne sont pas exécutés automatiquement; vous devez les exécuter explicitement pour générer des données de sortie.</span><span class="sxs-lookup"><span data-stu-id="816e1-112">Reports are not run automatically; you must run them explicitly to generate output data.</span></span> <span data-ttu-id="816e1-113">La durée nécessaire à l’exécution de ce rapport dépend de la quantité de données collectées dans le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="816e1-113">The length of time it takes to run this report is determined by the amount of data collected in the data store.</span></span>

<span data-ttu-id="816e1-114">Après avoir exécuté un rapport et que la sortie est affichée dans la console de gestion du serveur d’applications, vous pouvez exporter le rapport dans les formats suivants:</span><span class="sxs-lookup"><span data-stu-id="816e1-114">After you run a report and the output is displayed in the Application Virtualization Server Management Console, you can export the report into the following formats:</span></span>

-   <span data-ttu-id="816e1-115">Adobe Acrobat (PDF)</span><span class="sxs-lookup"><span data-stu-id="816e1-115">Adobe Acrobat (PDF)</span></span>

-   <span data-ttu-id="816e1-116">Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="816e1-116">Microsoft Office Excel</span></span>

<span data-ttu-id="816e1-117">**Remarques**  Le nom de serveur App-V indiqué auprès des clients doit faire partie du groupe de serveurs par défaut afin que le rapport sur l’utilisation du système affiche les données.</span><span class="sxs-lookup"><span data-stu-id="816e1-117">**Note** The App-V server name reported from the clients must be part of the Default Server Group in order for the System Utilization report to show data.</span></span> <span data-ttu-id="816e1-118">Par exemple, si vous utilisez plusieurs serveurs avec un équilibrage de charge réseau, vous devez ajouter le nom de cluster NLB au groupe de serveurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="816e1-118">For example, if you are using multiple servers with a Network Load Balancer (NLB), you must add the NLB cluster name to the Default Server Group.</span></span>

 

## <span data-ttu-id="816e1-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="816e1-119">Related topics</span></span>


[<span data-ttu-id="816e1-120">Procédure pour créer un rapport</span><span class="sxs-lookup"><span data-stu-id="816e1-120">How to Create a Report</span></span>](how-to-create-a-reportserver.md)

[<span data-ttu-id="816e1-121">Procédure pour supprimer un rapport</span><span class="sxs-lookup"><span data-stu-id="816e1-121">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)

[<span data-ttu-id="816e1-122">Procédure pour exporter un rapport</span><span class="sxs-lookup"><span data-stu-id="816e1-122">How to Export a Report</span></span>](how-to-export-a-reportserver.md)

[<span data-ttu-id="816e1-123">Procédure pour imprimer un rapport</span><span class="sxs-lookup"><span data-stu-id="816e1-123">How to Print a Report</span></span>](how-to-print-a-reportserver.md)

[<span data-ttu-id="816e1-124">Procédure pour exécuter un rapport</span><span class="sxs-lookup"><span data-stu-id="816e1-124">How to Run a Report</span></span>](how-to-run-a-reportserver.md)

 

 





