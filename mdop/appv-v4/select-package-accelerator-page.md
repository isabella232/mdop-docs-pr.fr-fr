---
title: Page Sélectionner un accélérateur de package
description: Page Sélectionner un accélérateur de package
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806369"
---
# <span data-ttu-id="b0be8-103">Page Sélectionner un accélérateur de package</span><span class="sxs-lookup"><span data-stu-id="b0be8-103">Select Package Accelerator Page</span></span>


<span data-ttu-id="b0be8-104">Servez-vous de la page **Sélectionner l’accélérateur de package** pour sélectionner l’accélérateur de package à utiliser pour créer le package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b0be8-104">Use the **Select Package Accelerator** page to select the Package Accelerator that will be used to create the new virtual application package.</span></span> <span data-ttu-id="b0be8-105">Vous devez copier l’accélérateur de package vers un dossier sur l’ordinateur exécutant le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="b0be8-105">You must copy the Package Accelerator to a folder on the computer running the App-V Sequencer.</span></span> <span data-ttu-id="b0be8-106">Pour plus d’informations, voir [à propos des accélérateurs de package App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="b0be8-106">For more information, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="b0be8-107">Exécutez uniquement les accélérateurs de package d’éditeurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="b0be8-107">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="b0be8-108">Les accélérateurs de package incluent généralement une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="b0be8-108">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="b0be8-109">Une signature numérique est une marque de sécurité électronique qui peut vous aider à indiquer l’éditeur du logiciel et si le package a été falsifié après la signature initiale de la transformation.</span><span class="sxs-lookup"><span data-stu-id="b0be8-109">A digital signature is an electronic security mark that can help indicate the publisher of the software, and whether the package has been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="b0be8-110">Si vous utilisez une transformation qui a été signée numériquement par un éditeur et que l’éditeur a vérifié son identité auprès d’une autorité de certification, vous pouvez être sûr que la transformation provient d’un éditeur spécifique et qu’elle n’a pas été altérée.</span><span class="sxs-lookup"><span data-stu-id="b0be8-110">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="b0be8-111">Le Sequencer App-V vous avertit si l’une des conditions suivantes est vraie:</span><span class="sxs-lookup"><span data-stu-id="b0be8-111">The App-V Sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="b0be8-112">La transformation sélectionnée n’a pas été signée numériquement.</span><span class="sxs-lookup"><span data-stu-id="b0be8-112">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="b0be8-113">La transformation sélectionnée est signée par un éditeur qui n’a pas vérifié son identité auprès d’une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="b0be8-113">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="b0be8-114">La transformation sélectionnée a été modifiée après sa signature numérique et sa sortie.</span><span class="sxs-lookup"><span data-stu-id="b0be8-114">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="b0be8-115">Si l’un de ces messages s’affiche lors de l’utilisation d’un accélérateur de package, rendez-vous sur le site Web de l’éditeur accélérateurs de packages pour obtenir une version signée numériquement de la transformation.</span><span class="sxs-lookup"><span data-stu-id="b0be8-115">If any of these messages are displayed when using a Package Accelerators, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

<span data-ttu-id="b0be8-116">Cette page contient les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="b0be8-116">This page contains the following elements:</span></span>

<a href="" id="browse"></a>**<span data-ttu-id="b0be8-117">Parcourir</span><span class="sxs-lookup"><span data-stu-id="b0be8-117">Browse</span></span>**  
<span data-ttu-id="b0be8-118">Cliquez sur **Parcourir** pour spécifier l’accélérateur de package à utiliser pour créer le package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b0be8-118">Click **Browse** to specify the Package Accelerator that you will use to create the virtual application package.</span></span> <span data-ttu-id="b0be8-119">Enregistrez l’accélérateur de package que vous avez spécifié localement sur l’ordinateur exécutant le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="b0be8-119">Save the Package Accelerator you specified locally on the computer that is running the Sequencer.</span></span>

## <span data-ttu-id="b0be8-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0be8-120">Related topics</span></span>


[<span data-ttu-id="b0be8-121">Assistant Sequencer - Accélérateur de package (AppV4.6SP1)</span><span class="sxs-lookup"><span data-stu-id="b0be8-121">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





