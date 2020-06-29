---
title: Redémarrage et réinitialisation d'un espace de travail MED-V
description: Redémarrage et réinitialisation d'un espace de travail MED-V
author: dansimp
ms.assetid: a959cdb3-a727-47c7-967e-e58f224e74de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48a644c2ed1668f87eb6e1a78521e780e8b783dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811147"
---
# <span data-ttu-id="138fc-103">Redémarrage et réinitialisation d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="138fc-103">Restarting and Resetting a MED-V Workspace</span></span>


<span data-ttu-id="138fc-104">Lors de la résolution des problèmes, vous pouvez parfois être amené à redémarrer ou Réinitialier l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="138fc-104">During troubleshooting, you may sometimes find it necessary to restart or reset the MED-V workspace.</span></span> <span data-ttu-id="138fc-105">Le redémarrage de l’espace de travail MED-V est essentiellement le même que le redémarrage d’un ordinateur physique.</span><span class="sxs-lookup"><span data-stu-id="138fc-105">Restarting the MED-V workspace is basically the same as restarting a physical computer.</span></span> <span data-ttu-id="138fc-106">La réinitialisation de l’espace de travail MED-V réexécute le programme d’installation pour la première fois et supprime toutes les données stockées dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="138fc-106">Resetting the MED-V workspace reruns first time setup and deletes all data that is stored in the virtual machine.</span></span> <span data-ttu-id="138fc-107">Dans la mesure où toutes les données stockées sont supprimées, vous devez généralement réinitialiser uniquement l’espace de travail MED-V pour résoudre les problèmes de résolution des problèmes les plus importants, ou restaurer un espace de travail MED-V qui fonctionne à nouveau dans un état de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="138fc-107">Because all stored data is deleted, you typically should only reset the MED-V workspace to resolve the most serious troubleshooting issues, or to restore a previously working MED-V workspace back to a working state.</span></span>

<span data-ttu-id="138fc-108">Pour plus d’informations sur l’ouverture du kit de tâches d’administration MED-V, voir [résolution des problèmes de med-v à l’aide du kit de tâches d’administration](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="138fc-108">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

**<span data-ttu-id="138fc-109">Redémarrage d’un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="138fc-109">Restarting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="138fc-110">Dans la fenêtre **Kit de tâches d’administration de med-v** , cliquez sur redémarrer l' **espace de travail MED-v**.</span><span class="sxs-lookup"><span data-stu-id="138fc-110">On the **MED-V Administration Toolkit** window, click **Restart MED-V Workspace**.</span></span> <span data-ttu-id="138fc-111">Une fenêtre de boîte de dialogue s’ouvre, dans laquelle vous devez confirmer que vous voulez redémarrer l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="138fc-111">A dialog window opens in which you must confirm that you want to restart the MED-V workspace.</span></span>

2.  <span data-ttu-id="138fc-112">Cliquez sur **redémarrer**.</span><span class="sxs-lookup"><span data-stu-id="138fc-112">Click **Restart**.</span></span>

    <span data-ttu-id="138fc-113">Toutes les applications publiées en cours d’exécution ou les sites Web redirigés qui sont ouvertes seront fermés lors du redémarrage de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="138fc-113">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace restarts.</span></span>

**<span data-ttu-id="138fc-114">Réinitialisation d’un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="138fc-114">Resetting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="138fc-115">Dans la fenêtre **Kit de tâches d’administration de med-v** , cliquez sur Réinitialiser l' **espace de travail MED-v**.</span><span class="sxs-lookup"><span data-stu-id="138fc-115">On the **MED-V Administration Toolkit** window, click **Reset MED-V Workspace**.</span></span> <span data-ttu-id="138fc-116">Une fenêtre de boîte de dialogue s’ouvre, dans laquelle vous devez confirmer la réinitialisation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="138fc-116">A dialog window opens in which you must confirm that you want to reset the MED-V workspace.</span></span>

    <span data-ttu-id="138fc-117">**Avertissement**  La réinitialisation de l’espace de travail MED-V entraîne une nouvelle exécution du programme d’installation, et recharge par conséquent le disque dur virtuel d’origine.</span><span class="sxs-lookup"><span data-stu-id="138fc-117">**Warning** Resetting the MED-V workspace causes first time setup to run again, and thus reloads the original virtual hard disk.</span></span> <span data-ttu-id="138fc-118">Toutes les données stockées dans l’espace de travail MED-V depuis la première exécution seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="138fc-118">All data that is stored in the MED-V workspace since first time setup was originally run will be deleted.</span></span>

     

2.  <span data-ttu-id="138fc-119">Cliquez sur **Réinitialiser**.</span><span class="sxs-lookup"><span data-stu-id="138fc-119">Click **Reset**.</span></span>

    <span data-ttu-id="138fc-120">Toutes les applications publiées en cours d’exécution ou les sites Web redirigés qui sont ouvertes seront fermés lors de la réinitialisation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="138fc-120">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace resets.</span></span>

## <span data-ttu-id="138fc-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="138fc-121">Related topics</span></span>


[<span data-ttu-id="138fc-122">Affichage et configuration des journaux MED-V</span><span class="sxs-lookup"><span data-stu-id="138fc-122">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)

[<span data-ttu-id="138fc-123">Affichage des configurations d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="138fc-123">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





