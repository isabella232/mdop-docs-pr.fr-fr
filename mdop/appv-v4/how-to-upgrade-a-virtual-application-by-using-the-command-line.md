---
title: Procédure pour mettre à niveau une application virtuelle à l'aide de la ligne de commande
description: Procédure pour mettre à niveau une application virtuelle à l'aide de la ligne de commande
author: dansimp
ms.assetid: 83c97767-6ea1-42aa-b411-ccc9fa61cf81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8612deb31a1692dd85cfee88ca4b18cbc5ac2ab2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806717"
---
# <span data-ttu-id="37e15-103">Procédure pour mettre à niveau une application virtuelle à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="37e15-103">How to Upgrade a Virtual Application by Using the Command Line</span></span>


<span data-ttu-id="37e15-104">Utilisez la procédure suivante pour mettre à niveau une application virtuelle à l’aide d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="37e15-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span>

**<span data-ttu-id="37e15-105">Pour mettre à niveau une application virtuelle</span><span class="sxs-lookup"><span data-stu-id="37e15-105">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="37e15-106">Sur l’ordinateur exécutant le Sequencer Application Virtualization (App-V), ouvrez l’invite de commandes, sélectionnez **Démarrer**, **exécuter**, puis tapez **cmd**.</span><span class="sxs-lookup"><span data-stu-id="37e15-106">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="37e15-107">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="37e15-107">Click **OK**.</span></span>

2.  <span data-ttu-id="37e15-108">À l’invite de commandes, indiquez l’emplacement où le Sequencer App-V est installé.</span><span class="sxs-lookup"><span data-stu-id="37e15-108">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="37e15-109">Par exemple, à l’invite de commandes, vous pouvez taper ce qui suit: **CD C:\\Program Files\\Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="37e15-109">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="37e15-110">À l’invite de commandes, tapez la commande suivante, en remplaçant le texte entre guillemets par vos valeurs:</span><span class="sxs-lookup"><span data-stu-id="37e15-110">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="37e15-111">Remarque</span><span class="sxs-lookup"><span data-stu-id="37e15-111">Note</span></span>**  
    <span data-ttu-id="37e15-112">Vous pouvez spécifier des paramètres supplémentaires à l’aide de la ligne de commande, en fonction de la complexité de l’application que vous effectuez la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="37e15-112">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="37e15-113">Pour obtenir la liste complète des paramètres disponibles pour une utilisation avec le Sequencer App-V, voir [paramètres de ligne de commande du Sequencer](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37e15-113">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



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



4. <span data-ttu-id="37e15-114">Appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="37e15-114">Press **Enter**.</span></span>

## <span data-ttu-id="37e15-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37e15-115">Related topics</span></span>


[<span data-ttu-id="37e15-116">Comment créer ou mettre à niveau des applications virtuelles à l’aide du Sequencer App-V</span><span class="sxs-lookup"><span data-stu-id="37e15-116">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="37e15-117">Codes des erreurs de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="37e15-117">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="37e15-118">Paramètres de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="37e15-118">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









