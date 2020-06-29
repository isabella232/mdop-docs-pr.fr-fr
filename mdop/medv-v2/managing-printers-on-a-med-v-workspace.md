---
title: Gestion des imprimantes sur un espace de travail MED-V
description: Gestion des imprimantes sur un espace de travail MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811562"
---
# <span data-ttu-id="77c11-103">Gestion des imprimantes sur un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="77c11-103">Managing Printers on a MED-V Workspace</span></span>


<span data-ttu-id="77c11-104">Dans la version 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V), la redirection d’imprimante fournit aux utilisateurs finaux une expérience d’impression homogène entre l’ordinateur virtuel MED-V et l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="77c11-104">In Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, printer redirection provides end users with a consistent printing experience between the MED-V virtual machine and the host computer.</span></span>

<span data-ttu-id="77c11-105">Cette rubrique fournit des informations sur la gestion de l’impression dans un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="77c11-105">This topic provides information about how to manage printing in a MED-V workspace.</span></span>

## <span data-ttu-id="77c11-106">Gestion des imprimantes dans les espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="77c11-106">Managing Printers in MED-V Workspaces</span></span>


<span data-ttu-id="77c11-107">Dans la plupart des cas, MED-V gère automatiquement la redirection de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="77c11-107">In most cases, MED-V handles printer redirection automatically.</span></span> <span data-ttu-id="77c11-108">Après avoir configuré la première fois, MED-V identifie toutes les imprimantes réseau installées sur l’hôte, récupère les pilotes correspondants auprès du serveur d’impression réseau, et, le cas échéant, installe les pilotes pertinents dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="77c11-108">After first time setup finishes, MED-V identifies all network printers installed on the host, retrieves the corresponding drivers from the network print server, and if found, installs the relevant drivers in the MED-V workspace.</span></span> <span data-ttu-id="77c11-109">Une fois tous les pilotes trouvés et installés, MED-V réamorce l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="77c11-109">After all drivers are found and installed, MED-V reboots the MED-V workspace.</span></span> <span data-ttu-id="77c11-110">En général, une fois que l’espace de travail MED-V est redémarré, les imprimantes hôtes sont présentes et disponibles sur l’invité, en général quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="77c11-110">Only after the MED-V workspace restarts, the host printers are present and available on the guest, typically in a few minutes.</span></span>

<span data-ttu-id="77c11-111">**Remarques**  Si des applications sont exécutées sur l’espace de travail MED-V, l’utilisateur final est invité à laisser le redémarrage continuer ou à le différer jusqu’à ce qu’il soit plus tard.</span><span class="sxs-lookup"><span data-stu-id="77c11-111">**Note** If applications are running on the MED-V workspace, the end user is prompted to let the restart continue or postpone it until later.</span></span> <span data-ttu-id="77c11-112">Si aucune application n’est en cours d’exécution, le redémarrage est automatique et n’est pas présenté à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="77c11-112">If no applications are running, the restart is automatic and not shown to the end user.</span></span>

 

<span data-ttu-id="77c11-113">Chaque fois que l’application MED-V est redémarrée, elle vérifie si de nouvelles imprimantes sont installées sur l’hôte et, le cas échéant, récupère les pilotes correspondants à partir du serveur d’impression réseau et les installe sur l’invité.</span><span class="sxs-lookup"><span data-stu-id="77c11-113">Every time MED-V is re-started, it checks whether any new printers are installed on the host and, if found, retrieves the corresponding drivers from the network print server and installs them on the guest.</span></span> <span data-ttu-id="77c11-114">MED-V redémarre ensuite l’espace de travail MED-V comme la première fois que vous avez terminé la configuration.</span><span class="sxs-lookup"><span data-stu-id="77c11-114">MED-V then restarts the MED-V workspace just as when first time setup was completed.</span></span>

<span data-ttu-id="77c11-115">**Important**  Une fois les pilotes pertinents installés sur l’invité, les imprimantes ne deviennent visibles sur l’invité qu’après le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="77c11-115">**Important** After the relevant drivers are installed on the guest, the printers only become visible on the guest after the restart occurs.</span></span>

 

<span data-ttu-id="77c11-116">Si un pilote est introuvable ou n’est pas installé, il doit être installé manuellement sur l’invité pour que l’imprimante réseau soit disponible pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="77c11-116">If at any time a driver cannot be located or installed, it must be manually installed on the guest for the network printer to be available to the end user.</span></span>

<span data-ttu-id="77c11-117">La liste suivante fournit des recommandations supplémentaires:</span><span class="sxs-lookup"><span data-stu-id="77c11-117">The following list offers some additional guidance:</span></span>

<span data-ttu-id="77c11-118">**MED-V gère uniquement les imprimantes réseau**.</span><span class="sxs-lookup"><span data-stu-id="77c11-118">**MED-V only manages network printers**.</span></span> <span data-ttu-id="77c11-119">Les pilotes pour les imprimantes installées localement sur l’hôte ne sont pas automatiquement installés sur l’invité.</span><span class="sxs-lookup"><span data-stu-id="77c11-119">Drivers for printers that are installed locally on the host are not automatically installed on the guest.</span></span>

<span data-ttu-id="77c11-120">**MED-V installe uniquement les pilotes d’imprimante s’il existe sur le serveur d’impression**.</span><span class="sxs-lookup"><span data-stu-id="77c11-120">**MED-V only installs printer drivers if found on the print server**.</span></span> <span data-ttu-id="77c11-121">Si ce n’est pas le cas, les pilotes d’imprimante doivent être installés manuellement.</span><span class="sxs-lookup"><span data-stu-id="77c11-121">If not found, printer drivers must be manually installed.</span></span>

<span data-ttu-id="77c11-122">**Les imprimantes installées manuellement sur l’invité ne sont pas accessibles à l’hôte**.</span><span class="sxs-lookup"><span data-stu-id="77c11-122">**Printers manually installed on the guest are not accessible to the host**.</span></span> <span data-ttu-id="77c11-123">Par défaut, la fonction MED-V ne prend en charge que la redirection d’imprimante de l’invité vers l’hôte.</span><span class="sxs-lookup"><span data-stu-id="77c11-123">By default, MED-V only supports printer redirection from the guest to the host.</span></span>

<span data-ttu-id="77c11-124">**Avertissement**  Si une imprimante est installée manuellement sur l’invité et qu’elle est installée plus tard sur l’hôte, il en résulte que l’imprimante est installée à deux reprises dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="77c11-124">**Warning** If a printer is manually installed on the guest, and the same printer is later installed on the host, the result is that the printer is installed two times in the guest.</span></span> <span data-ttu-id="77c11-125">Pour éviter ce problème, une meilleure pratique MED-V consiste à gérer la redirection de l’impression d’une manière uniquement: désactivez la redirection et l’installation manuelle de l’imprimante sur l’invité, ou activez la redirection et n’installez pas les imprimantes manuellement sur l’invité.</span><span class="sxs-lookup"><span data-stu-id="77c11-125">To avoid this situation, a MED-V best practice is to manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

 

## <span data-ttu-id="77c11-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77c11-126">Related topics</span></span>


[<span data-ttu-id="77c11-127">Gérer les paramètres de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="77c11-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





