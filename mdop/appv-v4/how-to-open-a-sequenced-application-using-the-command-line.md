---
title: Procédure pour ouvrir une application séquencée à l'aide de la ligne de commande
description: Procédure pour ouvrir une application séquencée à l'aide de la ligne de commande
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806898"
---
# <span data-ttu-id="709d6-103">Procédure pour ouvrir une application séquencée à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="709d6-103">How to Open a Sequenced Application Using the Command Line</span></span>


<span data-ttu-id="709d6-104">Vous pouvez ouvrir des packages d’application virtuelle à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="709d6-104">You can open virtual application packages using the command line.</span></span> <span data-ttu-id="709d6-105">Vous devez exécuter l’invite **cmd** en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="709d6-105">You must run the **cmd** prompt as an administrator.</span></span>

<span data-ttu-id="709d6-106">Utilisez la procédure suivante pour ouvrir des packages d’application séquencés à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="709d6-106">Use the following procedure to open sequenced application packages using the command line</span></span>

**<span data-ttu-id="709d6-107">Pour ouvrir une application séquencée à l’aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="709d6-107">To open a sequenced application using the command line</span></span>**

1.  <span data-ttu-id="709d6-108">Pour ouvrir l’invite de commandes, cliquez sur **Démarrer**, sélectionnez **exécuter**, tapez **cmd**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="709d6-108">To open the command prompt, click **Start**, and select **Run**, type **cmd**, and click **OK**.</span></span>

2.  <span data-ttu-id="709d6-109">À l’invite de commandes, tapez **cd\\** et spécifiez le chemin d’accès au répertoire dans lequel le Sequencer est installé, puis appuyez sur **entrée.**</span><span class="sxs-lookup"><span data-stu-id="709d6-109">At a command prompt, type **cd\\** and specify the path to the directory where the Sequencer is installed and then press **Enter.**</span></span>

3.  <span data-ttu-id="709d6-110">À l’invite de commandes, tapez la commande suivante, en remplaçant le texte en italique par vos valeurs:</span><span class="sxs-lookup"><span data-stu-id="709d6-110">At the command prompt, type the following command, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="709d6-111">SFTSequencer/OPEN:*"spécifie le fichier. sprj à ouvrir"*</span><span class="sxs-lookup"><span data-stu-id="709d6-111">SFTSequencer /OPEN:*”specifies the .sprj file to open"*</span></span>

    <span data-ttu-id="709d6-112">Appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="709d6-112">Press **Enter**.</span></span>

4.  <span data-ttu-id="709d6-113">Vous pouvez également spécifier les paramètres facultatifs suivants.</span><span class="sxs-lookup"><span data-stu-id="709d6-113">You can also specify the following optional parameters.</span></span> <span data-ttu-id="709d6-114">À l’invite de commandes, tapez les commandes suivantes en remplaçant le texte en italique par vos valeurs:</span><span class="sxs-lookup"><span data-stu-id="709d6-114">At the command prompt, type the following commands, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="709d6-115">/PACKAGENAME: "*spécifie le nom du package"*</span><span class="sxs-lookup"><span data-stu-id="709d6-115">/PACKAGENAME:"*specifies the package name"*</span></span>

    <span data-ttu-id="709d6-116">/MSI: indique la génération d’un programme d’installation Microsoft Windows associé.</span><span class="sxs-lookup"><span data-stu-id="709d6-116">/MSI - specifies generating an associated Microsoft Windows Installer.</span></span>

    <span data-ttu-id="709d6-117">/COMPRESS: indique si le package est compressé.</span><span class="sxs-lookup"><span data-stu-id="709d6-117">/COMPRESS – specifies if the package will be compressed.</span></span> <span data-ttu-id="709d6-118">Par défaut, les packages ne sont pas compressés.</span><span class="sxs-lookup"><span data-stu-id="709d6-118">By default, packages are not compressed.</span></span>

    <span data-ttu-id="709d6-119">Appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="709d6-119">Press **Enter**.</span></span>

    <span data-ttu-id="709d6-120">**Remarques**  Si le programme d’installation ou le package Windows Installer possède une interface utilisateur graphique, il s’affiche lorsque vous spécifiez les paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="709d6-120">**Note** If the installer or Windows Installer package has a graphical user interface, it will be displayed after you specify the command-line parameters.</span></span>

     

## <span data-ttu-id="709d6-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="709d6-121">Related topics</span></span>


[<span data-ttu-id="709d6-122">Procédure pour gérer toutes les applications virtuelles à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="709d6-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





