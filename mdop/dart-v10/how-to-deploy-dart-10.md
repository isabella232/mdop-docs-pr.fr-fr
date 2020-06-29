---
title: Procédure de déploiement de DaRT10
description: Procédure de déploiement de DaRT10
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804704"
---
# <span data-ttu-id="d528c-103">Procédure de déploiement de DaRT10</span><span class="sxs-lookup"><span data-stu-id="d528c-103">How to Deploy DaRT 10</span></span>


<span data-ttu-id="d528c-104">Les instructions suivantes décrivent le déploiement de Microsoft Diagnostics and Recovery Tools (DaRT) 10 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="d528c-104">The following instructions explain how to deploy Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="d528c-105">Pour obtenir le logiciel DaRT, reportez-vous à la rubrique [obtention de MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="d528c-105">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span> <span data-ttu-id="d528c-106">Il est supposé que vous installez toutes les fonctionnalités sur un ordinateur d’administration.</span><span class="sxs-lookup"><span data-stu-id="d528c-106">It is assumed that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="d528c-107">Si vous devez déployer ou désinstaller DaRT 10 sur plusieurs ordinateurs, par exemple à l’aide d’un système de distribution de logiciels électronique, il peut s’avérer plus simple d’utiliser les options d’installation de lignes de commande.</span><span class="sxs-lookup"><span data-stu-id="d528c-107">If you need to deploy or uninstall DaRT 10 on multiple computers, using an electronic software distribution system, for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="d528c-108">Les descriptions et exemples des options de ligne de commande disponibles sont fournis dans cette section.</span><span class="sxs-lookup"><span data-stu-id="d528c-108">Descriptions and examples of the available command line options are provided in this section.</span></span>

<span data-ttu-id="d528c-109">**Important**  Avant d’installer DaRT, voir [Configurations prises en charge par DART 10](dart-10-supported-configurations.md) pour vérifier que vous avez installé tous les logiciels requis et que votre ordinateur dispose de la configuration minimale requise.</span><span class="sxs-lookup"><span data-stu-id="d528c-109">**Important** Before you install DaRT, see [DaRT 10 Supported Configurations](dart-10-supported-configurations.md) to ensure that you have installed all of the prerequisite software and that the computer meets the minimum system requirements.</span></span> <span data-ttu-id="d528c-110">L’ordinateur sur lequel vous installez DaRT doit exécuter Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d528c-110">The computer onto which you install DaRT must be running Windows 10.</span></span>

 

<span data-ttu-id="d528c-111">Vous pouvez installer DaRT en utilisant l’une des deux configurations suivantes:</span><span class="sxs-lookup"><span data-stu-id="d528c-111">You can install DaRT using one of two different configurations:</span></span>

-   <span data-ttu-id="d528c-112">Installez DaRT et tous les outils DaRT sur l’ordinateur d’administration.</span><span class="sxs-lookup"><span data-stu-id="d528c-112">Install DaRT and all of the DaRT tools on the administrator computer.</span></span>

-   <span data-ttu-id="d528c-113">Installez uniquement sur l’ordinateur d’administration les outils dont vous avez besoin pour créer l’image de récupération DaRT, puis installez la **visionneuse de connexions à distance** et, éventuellement, l' **analyseur d’incidents** sur un ordinateur de bureau d’assistance.</span><span class="sxs-lookup"><span data-stu-id="d528c-113">Install on the administrator computer only the tools that you need to create the DaRT recovery image, and then install the **Remote Connection Viewer** and, optionally, **Crash Analyzer** on a help desk computer.</span></span>

<span data-ttu-id="d528c-114">Le fichier d’installation DaRT est disponible dans les versions 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d528c-114">The DaRT installation file is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="d528c-115">Installez la version qui correspond à l’architecture de l’ordinateur sur lequel vous exécutez l’Assistant image de récupération DaRT, et non l’architecture informatique de l’image de récupération que vous créez.</span><span class="sxs-lookup"><span data-stu-id="d528c-115">Install the version that matches the architecture of the computer on which you are running the DaRT Recovery Image wizard, not the computer architecture of the recovery image that you are creating.</span></span>

<span data-ttu-id="d528c-116">Vous pouvez utiliser l’une des versions du fichier d’installation de DaRT pour créer une image de récupération pour les ordinateurs 32 ou 64, mais vous ne pouvez pas créer une image de récupération pour les ordinateurs 32-bits et 64.</span><span class="sxs-lookup"><span data-stu-id="d528c-116">You can use either version of the DaRT installation file to create a recovery image for either 32-bit or 64-bit computers, but you cannot create one recovery image for both 32-bit and 64-bit computers.</span></span>

**<span data-ttu-id="d528c-117">Pour installer DaRT et tous les outils DaRT sur un ordinateur d’administration</span><span class="sxs-lookup"><span data-stu-id="d528c-117">To install DaRT and all DaRT tools on an administrator computer</span></span>**

1.  <span data-ttu-id="d528c-118">Téléchargez la version 32 bits ou 64 bits du fichier d’installation de DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="d528c-118">Download the 32-bit or 64-bit version of the DaRT 10 installer file.</span></span> <span data-ttu-id="d528c-119">Choisissez l’architecture qui correspond à l’ordinateur sur lequel vous installez DaRT et exécutez l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="d528c-119">Choose the architecture that matches the computer on which you are installing DaRT and running the DaRT Recovery Image wizard.</span></span>

2.  <span data-ttu-id="d528c-120">À partir du dossier dans lequel vous avez téléchargé DaRT 10, exécutez le fichier d’installation **MSDaRT.msi** correspondant à votre configuration système requise.</span><span class="sxs-lookup"><span data-stu-id="d528c-120">From the folder into which you downloaded DaRT 10, run the **MSDaRT.msi** installation file that corresponds to your system requirements.</span></span>

3.  <span data-ttu-id="d528c-121">Dans la page **Bienvenue dans l’Assistant Configuration de Microsoft DART 10** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d528c-121">On the **Welcome to the Microsoft DaRT 10 Setup Wizard** page, click **Next**.</span></span>

4.  <span data-ttu-id="d528c-122">Acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d528c-122">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

5.  <span data-ttu-id="d528c-123">Sur la page **Microsoft Update** , sélectionnez **utiliser Microsoft Update lorsque je recherche des mises à jour**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d528c-123">On the **Microsoft Update** page, select **Use Microsoft Update when I check for updates**, and then click **Next**.</span></span>

6.  <span data-ttu-id="d528c-124">Dans la page **Sélectionner un dossier d’installation** , sélectionnez un dossier ou cliquez sur **suivant** pour installer DART dans l’emplacement d’installation par défaut.</span><span class="sxs-lookup"><span data-stu-id="d528c-124">On the **Select Installation Folder** page, select a folder, or click **Next** to install DaRT in the default installation location.</span></span>

7.  <span data-ttu-id="d528c-125">Sur la page **options d’installation** , sélectionnez les fonctionnalités de DART que vous voulez installer ou cliquez sur **suivant** pour installer DART avec toutes les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d528c-125">On the **Setup Options** page, select the DaRT features that you want to install, or click **Next** to install DaRT with all of the features.</span></span>

8.  <span data-ttu-id="d528c-126">Pour démarrer l’installation, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="d528c-126">To start the installation, click **Install**.</span></span>

9.  <span data-ttu-id="d528c-127">Lorsque l’installation est terminée, cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="d528c-127">After the installation has completed successfully, click **Finish** to exit the wizard.</span></span>

## <span data-ttu-id="d528c-128">Pour installer DaRT et tous les outils DaRT sur un ordinateur d’administration à l’aide d’une invite de commandes</span><span class="sxs-lookup"><span data-stu-id="d528c-128">To install DaRT and all DaRT tools on an administrator computer by using a command prompt</span></span>


<span data-ttu-id="d528c-129">Lors de l’installation ou de la désinstallation de DaRT, vous avez la possibilité d’exécuter les fichiers d’installation à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="d528c-129">When you install or uninstall DaRT, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="d528c-130">Cette section décrit quelques exemples d’options différentes que vous pouvez spécifier lorsque vous installez ou désinstallez DaRT à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="d528c-130">This section describes some examples of different options that you can specify when you install or uninstall DaRT at the command prompt.</span></span>

<span data-ttu-id="d528c-131">L’exemple suivant montre comment installer toutes les fonctionnalités de DaRT.</span><span class="sxs-lookup"><span data-stu-id="d528c-131">The following example shows how to install all DaRT functionality.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="d528c-132">L’exemple suivant montre comment installer uniquement l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="d528c-132">The following example shows how to install only the DaRT Recovery Image wizard.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

<span data-ttu-id="d528c-133">L’exemple suivant montre comment installer uniquement l’analyseur d’incidents et la visionneuse de connexion à distance DaRT.</span><span class="sxs-lookup"><span data-stu-id="d528c-133">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

<span data-ttu-id="d528c-134">L’exemple suivant crée un journal d’installation pour le programme d’installation de Windows.</span><span class="sxs-lookup"><span data-stu-id="d528c-134">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="d528c-135">Cela est utile pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="d528c-135">This is valuable for debugging.</span></span>

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

<span data-ttu-id="d528c-136">**Remarques**  Vous pouvez ajouter/qn ou/qb pour effectuer une installation silencieuse.</span><span class="sxs-lookup"><span data-stu-id="d528c-136">**Note** You can add /qn or /qb to perform a silent installation.</span></span>

 

**<span data-ttu-id="d528c-137">Pour valider l’installation de DaRT</span><span class="sxs-lookup"><span data-stu-id="d528c-137">To validate the DaRT installation</span></span>**

1.  <span data-ttu-id="d528c-138">Cliquez sur **Démarrer**, puis sélectionnez **Diagnostics et outils de récupération**.</span><span class="sxs-lookup"><span data-stu-id="d528c-138">Click **Start**, and select **Diagnostics and Recovery Toolset**.</span></span>

    <span data-ttu-id="d528c-139">La fenêtre du **jeu d’outils de diagnostics et de récupération** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="d528c-139">The **Diagnostics and Recovery Toolset** window opens.</span></span>

2.  <span data-ttu-id="d528c-140">Vérifiez que tous les outils DaRT sélectionnés pour l’installation ont été correctement installés.</span><span class="sxs-lookup"><span data-stu-id="d528c-140">Check that all of the DaRT tools that you selected for installation were successfully installed.</span></span>

## <span data-ttu-id="d528c-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d528c-141">Related topics</span></span>


[<span data-ttu-id="d528c-142">Déploiement de DaRT10 sur les ordinateurs des administrateurs</span><span class="sxs-lookup"><span data-stu-id="d528c-142">Deploying DaRT 10 to Administrator Computers</span></span>](deploying-dart-10-to-administrator-computers.md)

 

 





