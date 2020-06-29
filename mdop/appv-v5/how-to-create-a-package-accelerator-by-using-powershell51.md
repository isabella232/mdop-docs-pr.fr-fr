---
title: Comment créer un accélérateur de package à l'aide de PowerShell
description: Comment créer un accélérateur de package à l'aide de PowerShell
author: dansimp
ms.assetid: 0cb98394-4477-4193-8c5f-1c1773c7263a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 347572343cff058a7494574035464d66c4d61be4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805610"
---
# <span data-ttu-id="8ea0a-103">Comment créer un accélérateur de package à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ea0a-103">How to Create a Package Accelerator by Using PowerShell</span></span>


<span data-ttu-id="8ea0a-104">Les accélérateurs de package App-V 5,1 séquencéssent automatiquement de grandes applications complexes.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-104">App-V 5.1 package accelerators automatically sequence large, complex applications.</span></span> <span data-ttu-id="8ea0a-105">Par ailleurs, lorsque vous appliquez un accélérateur de package App-V 5,1, il n’est pas toujours nécessaire d’installer manuellement une application pour créer le package virtualisé.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-105">Additionally, when you apply an App-V 5.1 package accelerator, you are not always required to manually install an application to create the virtualized package.</span></span>

**<span data-ttu-id="8ea0a-106">Pour créer un accélérateur de package</span><span class="sxs-lookup"><span data-stu-id="8ea0a-106">To create a package accelerator</span></span>**

1.  <span data-ttu-id="8ea0a-107">Installez le Sequencer App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="8ea0a-108">Pour plus d’informations sur l’installation de Sequencer, voir [Comment installer le Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="8ea0a-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="8ea0a-109">Pour ouvrir une console PowerShell, cliquez sur **Démarrer** et tapez **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="8ea0a-110">Cliquez avec le bouton droit sur **Windows PowerShell**, puis sélectionnez **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span> <span data-ttu-id="8ea0a-111">Utilisez l’applet **de nouvelle applet de nouveau-AppvPackageAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="8ea0a-111">Use the **New-AppvPackageAccelerator** cmdlet.</span></span>

3.  <span data-ttu-id="8ea0a-112">Pour créer un accélérateur de package, assurez-vous d’avoir le package. AppV pour créer un accélérateur à partir de, les fichiers de média d’installation ou d’installation, et éventuellement un fichier Lisez-moi pour les utilisateurs de l’accélérateur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-112">To create a package accelerator, make sure that you have the .appv package to create an accelerator from, the installation media or installation files, and optionally a read me file for consumers of the accelerator to use.</span></span> <span data-ttu-id="8ea0a-113">Les paramètres suivants sont requis pour utiliser l’applet de commande du package Accelerator:</span><span class="sxs-lookup"><span data-stu-id="8ea0a-113">The following parameters are required to use the package accelerator cmdlet:</span></span>

    -   <span data-ttu-id="8ea0a-114">**InstalledFilesPath** : spécifie le chemin d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-114">**InstalledFilesPath** - specifies the application installation path.</span></span>

    -   <span data-ttu-id="8ea0a-115">**Programme d’installation** : spécifie le chemin d’accès au support du programme d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-115">**Installer** – specifies the path to the application installer media</span></span>

    -   <span data-ttu-id="8ea0a-116">**InputPackagePath** : spécifie le chemin d’accès au package. AppV.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-116">**InputPackagePath** – specifies the path to the .appv package</span></span>

    -   <span data-ttu-id="8ea0a-117">**Path** : spécifie le répertoire de sortie du package.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-117">**Path** – specifies the output directory for the package.</span></span>

    <span data-ttu-id="8ea0a-118">L’exemple suivant montre comment créer un accélérateur de package avec un package. AppV et le support d’installation:</span><span class="sxs-lookup"><span data-stu-id="8ea0a-118">The following example displays how you can create a package accelerator with an .appv package and the installation media:</span></span>

    **<span data-ttu-id="8ea0a-119">New-AppvPackageAccelerator-InputPackagePath &lt; chemin d’accès au fichier. AppV &gt; -chemin du programme d’installation &lt; dans le répertoire exécutable du programme d’installation &gt; &lt; du chemin de sortie&gt;</span><span class="sxs-lookup"><span data-stu-id="8ea0a-119">New-AppvPackageAccelerator -InputPackagePath &lt;path to the .appv file&gt; -Installer &lt;path to the installer executable&gt; -Path &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="8ea0a-120">Les paramètres facultatifs supplémentaires qui peuvent être utilisés avec l’applet **de commande New-AppvPackageAccelerator** s’affichent dans la liste suivante:</span><span class="sxs-lookup"><span data-stu-id="8ea0a-120">Additional optional parameters that can be used with the **New-AppvPackageAccelerator** cmdlet are displayed in the following list:</span></span>

    -   <span data-ttu-id="8ea0a-121">**AcceleratorDescriptionFile** : spécifie le chemin d’accès aux instructions de l’accélérateur de package créé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-121">**AcceleratorDescriptionFile** - specifies the path to user created package accelerator instructions.</span></span> <span data-ttu-id="8ea0a-122">Les instructions de l’accélérateur de package sont des fichiers de description **. txt** ou **. rtf** qui seront empaquetés avec le package créé à l’aide de l’accélérateur de package.</span><span class="sxs-lookup"><span data-stu-id="8ea0a-122">The package accelerator instructions are **.txt** or **.rtf** description files that will be packaged with the package created using the package accelerator.</span></span>

    <span data-ttu-id="8ea0a-123">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="8ea0a-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="8ea0a-124">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="8ea0a-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="8ea0a-125">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="8ea0a-125">Got an App-V issue?</span></span>** <span data-ttu-id="8ea0a-126">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="8ea0a-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="8ea0a-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ea0a-127">Related topics</span></span>


[<span data-ttu-id="8ea0a-128">Administration d'App-V5.1 à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ea0a-128">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





