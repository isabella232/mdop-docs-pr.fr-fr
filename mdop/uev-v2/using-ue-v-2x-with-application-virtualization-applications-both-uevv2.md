---
title: Utilisation d’UE-V 2. x avec les applications de virtualisation des applications
description: Utilisation d’UE-V 2. x avec les applications de virtualisation des applications
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812257"
---
# <span data-ttu-id="907e9-103">Utilisation d’UE-V 2. x avec les applications de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="907e9-103">Using UE-V 2.x with Application Virtualization Applications</span></span>


<span data-ttu-id="907e9-104">Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 prennent en charge les applications Microsoft Application Virtualization (App-v) sans modification requise du package App-V ou du modèle UE-V.</span><span class="sxs-lookup"><span data-stu-id="907e9-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 support Microsoft Application Virtualization (App-V) applications without any required modifications to either the App-V package or the UE-V template.</span></span> <span data-ttu-id="907e9-105">Toutefois, une étape supplémentaire est nécessaire, car vous ne pouvez pas exécuter le générateur UE-V directement sur une application application-V virtualisée.</span><span class="sxs-lookup"><span data-stu-id="907e9-105">However, an additional step is required because you cannot run the UE-V Generator directly on a virtualized App-V application.</span></span> <span data-ttu-id="907e9-106">Au lieu de cela, vous devez installer l’application localement, générer le modèle, puis appliquer le modèle à l’application virtualisée.</span><span class="sxs-lookup"><span data-stu-id="907e9-106">Instead, you must install the application locally, generate the template, and then apply the template to the virtualized application.</span></span> <span data-ttu-id="907e9-107">UE-V prend en charge les packages App-v 4,5, App-V 4,6 et App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="907e9-107">UE-V supports App-V 4.5, App-V 4.6, and App-V 5.0 packages.</span></span>

## <span data-ttu-id="907e9-108">Synchronisation des paramètres d’UE-V pour les applications App-v</span><span class="sxs-lookup"><span data-stu-id="907e9-108">UE-V settings synchronization for App-V applications</span></span>


<span data-ttu-id="907e9-109">UE-V vérifie qu’une application s’ouvre à l’aide du nom du programme et, facultativement, des numéros de version des fichiers et des numéros de version des produits, que l’application soit installée en local ou virtuellement à l’aide de App-V.</span><span class="sxs-lookup"><span data-stu-id="907e9-109">UE-V monitors when an application opens by the program name and, optionally, by file version numbers and product version numbers, whether the application is installed locally or virtually by using App-V.</span></span> <span data-ttu-id="907e9-110">Au démarrage de l’application, UE-V surveille le processus App-V, applique les paramètres stockés dans le chemin de stockage des paramètres de l’utilisateur, puis permet à l’application de démarrer normalement.</span><span class="sxs-lookup"><span data-stu-id="907e9-110">When the application starts, UE-V monitors the App-V process, applies any settings that are stored in the user's settings storage path, and then enables the application to start normally.</span></span> <span data-ttu-id="907e9-111">Dans le cadre de l’utilisation des applications App-V, UE-V effectue une conversion automatique des chemins de fichier et du registre appropriés vers l’emplacement virtualisé plutôt que de l’emplacement physique hors de l’environnement d’application-V.</span><span class="sxs-lookup"><span data-stu-id="907e9-111">UE-V monitors App-V applications and automatically translates the relevant file and registry paths to the virtualized location as opposed to the physical location outside the App-V computing environment.</span></span>

 **<span data-ttu-id="907e9-112">Pour implémenter la synchronisation des paramètres pour une application virtualisée</span><span class="sxs-lookup"><span data-stu-id="907e9-112">To implement settings synchronization for a virtualized application</span></span>**

1.  <span data-ttu-id="907e9-113">Exécutez le générateur UE-V pour collecter les paramètres de l’application installée localement dont vous voulez synchroniser les paramètres entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="907e9-113">Run the UE-V Generator to collect the settings of the locally installed application whose settings you want to synchronize between computers.</span></span> <span data-ttu-id="907e9-114">Ce processus crée un modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="907e9-114">This process creates a settings location template.</span></span> <span data-ttu-id="907e9-115">Si vous utilisez un modèle intégré tel que le modèle Microsoft Office 2010, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="907e9-115">If you use a built-in template such as the Microsoft Office 2010 template, skip this step.</span></span> <span data-ttu-id="907e9-116">Pour plus d’informations sur l’exécution du générateur UE-V, voir [déployer UE-v 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span><span class="sxs-lookup"><span data-stu-id="907e9-116">For more information about running the UE-V Generator, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span></span>

2.  <span data-ttu-id="907e9-117">Si vous ne l’avez pas déjà fait, installez le package d’application App-V.</span><span class="sxs-lookup"><span data-stu-id="907e9-117">Install the App-V application package if you have not already done so.</span></span>

3.  <span data-ttu-id="907e9-118">Publiez le modèle à l’emplacement de votre catalogue de modèles de paramètres ou installez-le manuellement à l’aide de l’applet de la `Register-UEVTemplate` cmdlet Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="907e9-118">Publish the template to the location of your settings template catalog or manually install the template by using the `Register-UEVTemplate` Windows PowerShell cmdlet.</span></span>

    <span data-ttu-id="907e9-119">**Remarques**  Si vous publiez le modèle qui vient d’être créé dans le catalogue de modèles paramètres, le client ne reçoit pas le modèle tant que le fournisseur de synchronisation n’a pas mis à jour les paramètres.</span><span class="sxs-lookup"><span data-stu-id="907e9-119">**Note** If you publish the newly created template to the settings template catalog, the client does not receive the template until the sync provider updates the settings.</span></span> <span data-ttu-id="907e9-120">Pour démarrer manuellement le processus, ouvrez **le planificateur de tâches**, développez Bibliothèque du planificateur de **tâches**, développez **Microsoft**, puis **UE-V**.</span><span class="sxs-lookup"><span data-stu-id="907e9-120">To manually start this process, open **Task Scheduler**, expand **Task Scheduler Library**, expand **Microsoft**, and expand **UE-V**.</span></span> <span data-ttu-id="907e9-121">Dans le volet résultats, cliquez avec le bouton droit sur **mise à jour automatique de modèle**, puis cliquez sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="907e9-121">In the results pane, right-click **Template Auto Update**, and then click **Run**.</span></span>

     

4.  <span data-ttu-id="907e9-122">Démarrez le package App-V.</span><span class="sxs-lookup"><span data-stu-id="907e9-122">Start the App-V package.</span></span>






## <span data-ttu-id="907e9-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="907e9-123">Related topics</span></span>


[<span data-ttu-id="907e9-124">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="907e9-124">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





