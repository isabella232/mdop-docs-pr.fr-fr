---
title: Page Fichiers d'installation
description: Page Fichiers d'installation
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806669"
---
# <span data-ttu-id="2a652-103">Page Fichiers d'installation</span><span class="sxs-lookup"><span data-stu-id="2a652-103">Installation Files Page</span></span>


<span data-ttu-id="2a652-104">Utilisez la page **fichiers d’installation** pour spécifier les fichiers d’installation utilisés pour créer le package d’application virtuel spécifié dans la page Sélectionner un **package** de cet Assistant.</span><span class="sxs-lookup"><span data-stu-id="2a652-104">Use the **Installation Files** page to specify the installation files that were used to create the virtual application package specified on the **Select Package** page of this wizard.</span></span> <span data-ttu-id="2a652-105">Si vous avez créé un package d’application virtuel contenant plusieurs applications, vous devez copier tous les fichiers d’installation requis vers un dossier sur l’ordinateur exécutant le Sequencer Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="2a652-105">If you created a virtual application package that contains multiple applications, you should copy all required installation files to a single folder on the computer running the Microsoft Application Virtualization Sequencer.</span></span>

<span data-ttu-id="2a652-106">Cette page contient les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="2a652-106">This page contains the following elements:</span></span>

<a href="" id="original-installation-files"></a>**<span data-ttu-id="2a652-107">Fichiers d’installation d’origine</span><span class="sxs-lookup"><span data-stu-id="2a652-107">Original Installation Files</span></span>**  
<span data-ttu-id="2a652-108">Cliquez sur **Parcourir** pour spécifier les fichiers d’installation utilisés à l’origine pour créer le package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="2a652-108">Click **Browse** to specify the installation files that were originally used to create the virtual application package.</span></span> <span data-ttu-id="2a652-109">Le répertoire parent que vous spécifiez doit être enregistré localement sur l’ordinateur exécutant le Sequencer et doit contenir tous les fichiers d’installation requis ou les sous-dossiers contenant les fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="2a652-109">The parent directory you specify should be saved locally to the computer running the Sequencer and must contain all required installation files or subfolders that contain the installation files.</span></span> <span data-ttu-id="2a652-110">Les fichiers d’installation peuvent être contenus dans le dossier parent ou dans un sous-dossier du dossier parent spécifié.</span><span class="sxs-lookup"><span data-stu-id="2a652-110">The installation files can be contained in the parent folder or in any of the subfolders of the specified parent folder.</span></span>

<a href="" id="files-installed-on-local-system"></a>**<span data-ttu-id="2a652-111">Fichiers installés sur le système local</span><span class="sxs-lookup"><span data-stu-id="2a652-111">Files installed on local system</span></span>**  
<span data-ttu-id="2a652-112">Cliquez sur **Parcourir** pour spécifier les fichiers d’installation installés localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2a652-112">Click **Browse** to specify the installation files that have been installed locally on the computer running the Sequencer.</span></span> <span data-ttu-id="2a652-113">Vous ne pouvez sélectionner cette option que si les fichiers d’installation de l’application ont été installés à l’emplacement par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="2a652-113">You can only select this option if the application installation files have been installed to the application’s default location.</span></span>

<span data-ttu-id="2a652-114">**Remarques**  L’emplacement d’installation par défaut que vous fournissez dépend des conditions suivantes:</span><span class="sxs-lookup"><span data-stu-id="2a652-114">**Note** The default installation location you provide depends on the following conditions:</span></span>

 

-   <span data-ttu-id="2a652-115">Racine du package spécifié lors de la création du package.</span><span class="sxs-lookup"><span data-stu-id="2a652-115">The package root specified when the package was originally created.</span></span>

-   <span data-ttu-id="2a652-116">Emplacement d’installation spécifié dans le programme d’installation Windows lors de la création du package.</span><span class="sxs-lookup"><span data-stu-id="2a652-116">The installation location specified in the Windows Installer when the package was originally created.</span></span>

-   <span data-ttu-id="2a652-117">Le chemin d’installation de l’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a652-117">The default application installation path.</span></span>

<span data-ttu-id="2a652-118">Par exemple, si la racine du package spécifiée est **Q:\\Office12** et au cours de l’installation, l’emplacement d’installation par défaut est passé de **C:\\Program Files\\Office12** à **Q:\\Office12**, puis le chemin d’accès spécifié lors de la mise en attente doit être **C:\\Program Files\\Office 12**.</span><span class="sxs-lookup"><span data-stu-id="2a652-118">For example, if the package root specified is **Q:\\Office12** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Office12**, then the path specified during dehydration must be **C:\\Program Files\\Office 12**.</span></span>

<span data-ttu-id="2a652-119">Si la racine du package spécifiée est **Q:\\Microsoft** et au cours de l’installation, l’emplacement d’installation par défaut est changé de **C:\\Program Files\\Office12** en **Q:\\Microsoft\\Office12**, puis le chemin d’accès spécifié lors de la mise en attente doit être **C:\\Program Files**.</span><span class="sxs-lookup"><span data-stu-id="2a652-119">If the package root specified is **Q:\\Microsoft** and during installation, the default installation location is changed from **C:\\Program Files\\Office12** to **Q:\\Microsoft\\Office12**, then the path specified during dehydration must be **C:\\Program Files**.</span></span>

<span data-ttu-id="2a652-120">Lorsque vous créez un package à l’aide d’un accélérateur de package, chaque fichier dans le package, par exemple **Q:\\Office12\\file.txt** est disponible sur l’ordinateur local en remplaçant le **Q:\\Office12** racine du package par l’emplacement par défaut spécifié lors de la création de l’accélérateur de package (par exemple, **C:\\Program Files\\Office12**).</span><span class="sxs-lookup"><span data-stu-id="2a652-120">When you create a package using a package accelerator, each file in the package, for example **Q:\\Office12\\file.txt** is found on the local computer by replacing the package root **Q:\\Office12** with the default location specified when the Package Accelerator was created, for example, **C:\\Program Files\\Office12**.</span></span> <span data-ttu-id="2a652-121">Dans l’exemple précédent, le fichier doit se trouver dans **C:\\Program Files\\Office12\\file.txt**.</span><span class="sxs-lookup"><span data-stu-id="2a652-121">In the previous example, the file should be located in **C:\\Program Files\\Office12\\file.txt**.</span></span>

## <span data-ttu-id="2a652-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a652-122">Related topics</span></span>


[<span data-ttu-id="2a652-123">Assistant Créer un accélérateur de package (AppV4.6SP1)</span><span class="sxs-lookup"><span data-stu-id="2a652-123">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





