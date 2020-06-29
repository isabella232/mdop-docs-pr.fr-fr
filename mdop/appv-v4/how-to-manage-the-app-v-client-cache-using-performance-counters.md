---
title: Procédure pour gérer le cache d'App-V Client à l'aide des compteurs de performances
description: Procédure pour gérer le cache d'App-V Client à l'aide des compteurs de performances
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806985"
---
# <span data-ttu-id="55f43-103">Procédure pour gérer le cache d'App-V Client à l'aide des compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="55f43-103">How to Manage the App-V Client Cache Using Performance Counters</span></span>


<span data-ttu-id="55f43-104">Vous pouvez suivre la procédure ci-dessous pour déterminer la quantité d’espace libre disponible dans le cache du client de virtualisation des applications (App-V) en utilisant l’outil Performance Monitor pour afficher les informations sous forme graphique.</span><span class="sxs-lookup"><span data-stu-id="55f43-104">You can use the following procedure to determine how much free space is available in the Application Virtualization (App-V) client cache by using Performance Monitor to display the information graphically.</span></span> <span data-ttu-id="55f43-105">Ces informations sont capturées sur l’ordinateur client par le biais d’un compteur de performance appelé «App Virt Client cache», qui inclut les compteurs suivants: «taille du cache (Mo)», «mettre en cache l’espace disponible (Mo)» et «% Free Space».</span><span class="sxs-lookup"><span data-stu-id="55f43-105">This information is captured on the client computer by a performance counter called “App Virt Client Cache,” and it includes the following counters: “Cache size (MB),” “Cache free space (MB),” and “% free space.”</span></span>

**<span data-ttu-id="55f43-106">Pour déterminer l’utilisation de l’espace cache du client</span><span class="sxs-lookup"><span data-stu-id="55f43-106">To determine client cache space usage</span></span>**

1.  <span data-ttu-id="55f43-107">Ouvrez une invite de commandes en tant qu’administrateur ou cliquez sur **Démarrer**, **exécuter**, tapez **perfmon.exe**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="55f43-107">Open a command prompt as administrator, or click **Start**, **Run**, type **perfmon.exe**, and click **OK**.</span></span>

2.  <span data-ttu-id="55f43-108">En fonction du système d’exploitation Windows utilisé, cliquez sur l’outil Moniteur de performance ou moniteur système après l’ouverture de la fenêtre MMC.</span><span class="sxs-lookup"><span data-stu-id="55f43-108">Depending on the Windows operating system being used, click the Performance Monitor or System Monitor tool after the MMC window opens.</span></span>

3.  <span data-ttu-id="55f43-109">Pour ajouter des compteurs, cliquez avec le bouton droit sur la zone du graphique, puis sélectionnez **Ajouter des compteurs**.</span><span class="sxs-lookup"><span data-stu-id="55f43-109">To add counters, right-click the graph area and select **Add Counters**.</span></span>

4.  <span data-ttu-id="55f43-110">Cliquez sur la liste déroulante pour afficher la liste des compteurs disponibles, faites défiler pour trouver l' **application Virt du cache du client**, puis ajoutez les trois compteurs.</span><span class="sxs-lookup"><span data-stu-id="55f43-110">Click the drop-down to display the list of available counters, scroll to find **App Virt Client Cache**, and then add the three counters.</span></span>

    <span data-ttu-id="55f43-111">**Important**  Les compteurs de performance App-V sont implémentés dans une DLL 32 bits, de sorte que pour les voir, vous devez utiliser la commande suivante pour démarrer la version 32 bits de performance Monitor: **MMC/32 Perfmon. msc**.</span><span class="sxs-lookup"><span data-stu-id="55f43-111">**Important** The App-V performance counters are implemented in a 32-bit DLL, so to see them, you must use the following command to start the 32-bit version of Performance Monitor: **mmc /32 perfmon.msc**.</span></span> <span data-ttu-id="55f43-112">Cette commande doit être exécutée directement sur l’ordinateur surveillé et ne peut pas être utilisée pour surveiller un ordinateur distant exécutant un système d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="55f43-112">This command must be run directly on the computer being monitored and cannot be used to monitor a remote computer running a 64-bit operating system.</span></span>

     

## <span data-ttu-id="55f43-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55f43-113">Related topics</span></span>


[<span data-ttu-id="55f43-114">Procédure pour gérer toutes les applications virtuelles à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="55f43-114">How to Manage Virtual Applications by Using the Command Line</span></span>](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





