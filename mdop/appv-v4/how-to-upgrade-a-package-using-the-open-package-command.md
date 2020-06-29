---
title: Procédure pour mettre à niveau un package à l'aide de la commande Ouvrir un package
description: Procédure pour mettre à niveau un package à l'aide de la commande Ouvrir un package
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806738"
---
# <span data-ttu-id="5b5d0-103">Procédure pour mettre à niveau un package à l'aide de la commande Ouvrir un package</span><span class="sxs-lookup"><span data-stu-id="5b5d0-103">How to Upgrade a Package Using the Open Package Command</span></span>


<span data-ttu-id="5b5d0-104">Utiliser la commande ouvrir un package pour mettre à niveau ou appliquer une mise à jour à un package d’application séquencé.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-104">Use the Open Package command to upgrade or apply an update to a sequenced application package.</span></span> <span data-ttu-id="5b5d0-105">Lorsque vous mettez à niveau un package d’application virtuelle existant à l’aide de la ligne de commande, la version d’origine du fichier. SFT est supprimée.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-105">When you upgrade an existing virtual application package using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="5b5d0-106">Il est recommandé de sauvegarder le fichier. SFT associé avant de mettre à niveau le package à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-106">You should backup the associated .sft file before upgrading the package using the command line.</span></span>

**<span data-ttu-id="5b5d0-107">Pour mettre à niveau un package à l’aide de la commande ouvrir le package</span><span class="sxs-lookup"><span data-stu-id="5b5d0-107">To upgrade a package using the Open Package command</span></span>**

1.  <span data-ttu-id="5b5d0-108">Pour ouvrir le package qui sera mis à niveau, dans la console Application Virtualization (App-V), sélectionnez **fichier**, puis **ouvrez package pour la mise à niveau**.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-108">To open the package that will be upgraded, in the Application Virtualization (App-V) console select **File**, **Open Package for Upgrade**.</span></span> <span data-ttu-id="5b5d0-109">Dans la boîte de dialogue **ouvrir** , sélectionnez le package qui sera mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-109">In the **Open** dialog box, select the package that will be upgraded.</span></span>

2.  <span data-ttu-id="5b5d0-110">Pour démarrer l’Assistant **séquençage** , sélectionnez **Outils**, **Assistant séquençage**.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-110">To start the **Sequencing** wizard, select **Tools**, **Sequencing Wizard**.</span></span> <span data-ttu-id="5b5d0-111">Suivez les étapes de l’Assistant pour enregistrer la nouvelle application séquencée, sélectionnez **fichier**, puis **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-111">Complete the wizard applying the configuration changes, to save the new sequenced application, select **File**, **Save**.</span></span>

3.  <span data-ttu-id="5b5d0-112">Pour ajouter le numéro de version au nom du package, dans la console de Sequencer, sélectionnez **Outils**, **options**.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-112">To append the version number to the package name, in the Sequencer console, select **Tools**, **Options**.</span></span> <span data-ttu-id="5b5d0-113">Sélectionnez **Ajouter la version du package au nom du fichier**.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-113">Select **Append Package Version to Filename**.</span></span> <span data-ttu-id="5b5d0-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-114">Click **OK**.</span></span>

    <span data-ttu-id="5b5d0-115">**Important**  Il est essentiel de mettre à jour le nom du fichier avec la version du package pour terminer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="5b5d0-115">**Important** Updating the file name with the package version is essential to successfully completing the upgrade.</span></span>

     

## <span data-ttu-id="5b5d0-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b5d0-116">Related topics</span></span>


[<span data-ttu-id="5b5d0-117">Procédure pour gérer toutes les applications virtuelles à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="5b5d0-117">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





