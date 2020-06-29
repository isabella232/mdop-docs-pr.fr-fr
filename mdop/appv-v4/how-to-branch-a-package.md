---
title: Procédure pour ramifier un package
description: Procédure pour ramifier un package
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807382"
---
# <span data-ttu-id="deb1b-103">Procédure pour ramifier un package</span><span class="sxs-lookup"><span data-stu-id="deb1b-103">How to Branch a Package</span></span>


<span data-ttu-id="deb1b-104">Utilisez cette procédure pour modifier un package d’application séquencé existant de sorte que vous puissiez l’exécuter côte à côte avec le package d’application séquencé d’origine.</span><span class="sxs-lookup"><span data-stu-id="deb1b-104">Use this procedure to modify an existing sequenced application package so you can run it side-by-side with the original sequenced application package.</span></span> <span data-ttu-id="deb1b-105">Ce processus porte le nom de branchement.</span><span class="sxs-lookup"><span data-stu-id="deb1b-105">This process is called branching.</span></span> <span data-ttu-id="deb1b-106">Lorsque vous agencez un package d’application virtuelle, vous pouvez exécuter deux versions du même package.</span><span class="sxs-lookup"><span data-stu-id="deb1b-106">When you branch a virtual application package you are able to run two versions of the same package.</span></span> <span data-ttu-id="deb1b-107">Par exemple, vous pouvez appliquer un service pack à un package existant et l’exécuter côte à côte avec le package d’application virtuelle séquencé d’origine.</span><span class="sxs-lookup"><span data-stu-id="deb1b-107">For example, you can apply a service pack to an existing package, and run it side-by-side with the original sequenced virtual application package.</span></span>

<span data-ttu-id="deb1b-108">Utilisez la procédure suivante pour brancher un package d’application virtuelle séquencé.</span><span class="sxs-lookup"><span data-stu-id="deb1b-108">Use the following procedure to branch a sequenced virtual application package.</span></span>

**<span data-ttu-id="deb1b-109">Pour brancher un package d’application virtuelle séquencé</span><span class="sxs-lookup"><span data-stu-id="deb1b-109">To branch a sequenced virtual application package</span></span>**

1.  <span data-ttu-id="deb1b-110">Ouvrez le Sequencer Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="deb1b-110">Open the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="deb1b-111">Pour spécifier le répertoire de destination qui contient le package (. sprj) sur lequel vous voulez sélectionner un **fichier**, **ouvrez**l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="deb1b-111">To specify the destination directory that contains the package (.sprj) you want to branch select **File**, **Open**.</span></span>

2.  <span data-ttu-id="deb1b-112">Accédez au dossier qui contient l’application séquencée que vous envisagez de brancher et cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="deb1b-112">Navigate to the directory that contains the sequenced application you plan to branch and click **Open**.</span></span>

3.  <span data-ttu-id="deb1b-113">Pour enregistrer une copie du package, dans le Sequencer App-V, sélectionnez **fichier**, **Enregistrer sous**.</span><span class="sxs-lookup"><span data-stu-id="deb1b-113">To save a copy of the package, in the App-V Sequencer, select **File**, **Save As**.</span></span> <span data-ttu-id="deb1b-114">Spécifiez un nouveau nom unique et spécifiez un nouveau répertoire racine de package unique pour la copie du package.</span><span class="sxs-lookup"><span data-stu-id="deb1b-114">Specify a new, unique name, and specify a new unique package root directory for the copy of the package.</span></span> <span data-ttu-id="deb1b-115">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="deb1b-115">Click **Save**.</span></span>

    **<span data-ttu-id="deb1b-116">Important</span><span class="sxs-lookup"><span data-stu-id="deb1b-116">Important</span></span>**  
    <span data-ttu-id="deb1b-117">Vous devez spécifier un nouveau nom de package ou vous remplacerez la version existante du package.</span><span class="sxs-lookup"><span data-stu-id="deb1b-117">You must specify a new package name or you will overwrite the existing version of the package.</span></span>



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. <span data-ttu-id="deb1b-118">Après avoir enregistré la nouvelle version, vous pouvez appliquer les modifications de configuration requises et enregistrer les fichiers. ICO, OSD, SFT et SPRJ pour corriger l’emplacement sur le serveur Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="deb1b-118">After you save the new version you can apply the required configuration changes and save the associated ICO, OSD, SFT, and SPRJ files to correct location on the Application Virtualization (App-V) server.</span></span>

## <span data-ttu-id="deb1b-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="deb1b-119">Related topics</span></span>


[<span data-ttu-id="deb1b-120">Tâches pour Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="deb1b-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)









