---
title: Procédure pour modifier les propriétés du package
description: Procédure pour modifier les propriétés du package
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807349"
---
# <span data-ttu-id="34f59-103">Procédure pour modifier les propriétés du package</span><span class="sxs-lookup"><span data-stu-id="34f59-103">How to Change Package Properties</span></span>


<span data-ttu-id="34f59-104">Vous pouvez utiliser les procédures suivantes pour modifier le nom du package de virtualisation des applications et les commentaires qui lui sont associés.</span><span class="sxs-lookup"><span data-stu-id="34f59-104">You can use the following procedures to modify an Application Virtualization package name and its associated comments.</span></span>

<span data-ttu-id="34f59-105">Si c’est la première fois que le package a été créé, vous pouvez également modifier la taille du bloc de paramètre de séquençage, qui détermine la façon dont un package d’application séquencé est transmis à partir d’un serveur de virtualisation des applications vers un client de bureau de la virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="34f59-105">If this is the first time the package has been created, you can also change the sequencing parameter block size, which determines how a sequenced application package is streamed from an Application Virtualization Server to an Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="34f59-106">**Remarques**  Lorsque vous sélectionnez une taille de bloc, tenez compte de la taille du fichier SFT et de la bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="34f59-106">**Note** When selecting a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="34f59-107">Le flux d’un fichier dont la taille de blocs est plus petite prend plus de temps sur le réseau, mais il est plus gourmand en bande passante.</span><span class="sxs-lookup"><span data-stu-id="34f59-107">A file with a smaller block size takes longer to stream over the network, but it is less bandwidth intensive.</span></span> <span data-ttu-id="34f59-108">Les fichiers de tailles de blocs plus grandes peuvent être plus rapides, mais ils utilisent plus de bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="34f59-108">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="34f59-109">Dans le cadre de l’expérimentation, vous pouvez découvrir la taille maximale de bloc pour les applications en continu sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="34f59-109">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span>

 

<span data-ttu-id="34f59-110">Le reste des propriétés de package sous l’onglet **Propriétés** est généré automatiquement et ne peut pas être modifié sous cet onglet.</span><span class="sxs-lookup"><span data-stu-id="34f59-110">The remainder of the package properties on the **Properties** tab is automatically generated and cannot be modified on this tab.</span></span>

**<span data-ttu-id="34f59-111">Pour modifier le nom ou les commentaires du package</span><span class="sxs-lookup"><span data-stu-id="34f59-111">To change the package name or comments</span></span>**

1.  <span data-ttu-id="34f59-112">Cliquez sur l’onglet **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="34f59-112">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="34f59-113">Dans la zone de texte **nom du package** , entrez ou modifiez le nom unique utilisé pour le package, qui peut contenir plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="34f59-113">In the **Package Name** text box, enter or edit the single name used for the package, which can contain multiple applications.</span></span>

3.  <span data-ttu-id="34f59-114">Dans la zone de texte **Commentaires** , vous pouvez entrer ou modifier des commentaires.</span><span class="sxs-lookup"><span data-stu-id="34f59-114">In the **Comments** text box, optionally enter or edit any comments.</span></span> <span data-ttu-id="34f59-115">La meilleure pratique recommandée consiste à fournir des informations détaillées sur le package et le séquençage.</span><span class="sxs-lookup"><span data-stu-id="34f59-115">The suggested best practice is to provide detail information about the package and sequencing.</span></span>

4.  <span data-ttu-id="34f59-116">Dans le menu **fichier** , sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="34f59-116">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="34f59-117">Pour modifier la taille du bloc</span><span class="sxs-lookup"><span data-stu-id="34f59-117">To change the block size</span></span>**

1.  <span data-ttu-id="34f59-118">Cliquez sur l’onglet **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="34f59-118">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="34f59-119">Dans la liste déroulante **taille de bloc** , sélectionnez **4 Ko**, **16 ko**, **32 Ko**ou **64 Ko**.</span><span class="sxs-lookup"><span data-stu-id="34f59-119">On the **Block Size** drop-down list, select **4 KB**, **16 KB**, **32 KB**, or **64 KB**.</span></span>

3.  <span data-ttu-id="34f59-120">Dans le menu **fichier** , sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="34f59-120">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="34f59-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34f59-121">Related topics</span></span>


[<span data-ttu-id="34f59-122">À propos de l'onglet Propriétés</span><span class="sxs-lookup"><span data-stu-id="34f59-122">About the Properties Tab</span></span>](about-the-properties-tab.md)

[<span data-ttu-id="34f59-123">Console Sequencer</span><span class="sxs-lookup"><span data-stu-id="34f59-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





