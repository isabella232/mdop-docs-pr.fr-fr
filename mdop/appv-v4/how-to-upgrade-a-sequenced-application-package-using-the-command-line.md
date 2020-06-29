---
title: Procédure pour mettre à niveau un package d'application séquencée à l'aide d'une ligne de commande
description: Procédure pour mettre à niveau un package d'application séquencée à l'aide d'une ligne de commande
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806726"
---
# <span data-ttu-id="764fc-103">Procédure pour mettre à niveau un package d'application séquencée à l'aide d'une ligne de commande</span><span class="sxs-lookup"><span data-stu-id="764fc-103">How to Upgrade a Sequenced Application Package Using the Command Line</span></span>


<span data-ttu-id="764fc-104">Utilisez la procédure suivante pour mettre à niveau une application virtuelle à l’aide d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="764fc-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span> <span data-ttu-id="764fc-105">Lorsque vous mettez à niveau un package d’application virtuelle existant à l’aide de la ligne de commande, la version d’origine du fichier. SFT est supprimée.</span><span class="sxs-lookup"><span data-stu-id="764fc-105">When you upgrade an existing virtual application package by using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="764fc-106">Vous devez sauvegarder le fichier. SFT associé avant de mettre à niveau le package à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="764fc-106">You should back up the associated .sft file before upgrading the package by using the command line.</span></span>

**<span data-ttu-id="764fc-107">Pour mettre à niveau une application virtuelle</span><span class="sxs-lookup"><span data-stu-id="764fc-107">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="764fc-108">Sur l’ordinateur exécutant le Sequencer Application Virtualization (App-V), ouvrez l’invite de commandes, sélectionnez **Démarrer**, **exécuter**, puis tapez **cmd**.</span><span class="sxs-lookup"><span data-stu-id="764fc-108">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="764fc-109">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="764fc-109">Click **OK**.</span></span>

2.  <span data-ttu-id="764fc-110">À l’invite de commandes, indiquez l’emplacement où le Sequencer App-V est installé.</span><span class="sxs-lookup"><span data-stu-id="764fc-110">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="764fc-111">Par exemple, à l’invite de commandes, vous pouvez taper ce qui suit: **CD C:\\Program Files\\Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="764fc-111">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="764fc-112">À l’invite de commandes, tapez la commande suivante, en remplaçant le texte entre guillemets par vos valeurs:</span><span class="sxs-lookup"><span data-stu-id="764fc-112">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="764fc-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="764fc-113">Note</span></span>**  
    <span data-ttu-id="764fc-114">Vous pouvez spécifier des paramètres supplémentaires à l’aide de la ligne de commande, en fonction de la complexité de l’application que vous effectuez la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="764fc-114">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="764fc-115">Pour obtenir la liste complète des paramètres disponibles pour une utilisation avec le Sequencer App-V, voir [paramètres de ligne de commande](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="764fc-115">For a complete list of parameters that are available for use with the App-V Sequencer, see [Command-Line Parameters](command-line-parameters.md).</span></span>



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="764fc-116">Appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="764fc-116">Press **Enter**.</span></span>

## <span data-ttu-id="764fc-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="764fc-117">Related topics</span></span>


[<span data-ttu-id="764fc-118">Procédure pour gérer toutes les applications virtuelles à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="764fc-118">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









