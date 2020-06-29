---
title: Procédure pour séquencer une nouvelle application à l'aide de la ligne de commande
description: Procédure pour séquencer une nouvelle application à l'aide de la ligne de commande
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806806"
---
# <span data-ttu-id="e8804-103">Procédure pour séquencer une nouvelle application à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="e8804-103">How to Sequence a New Application by Using the Command Line</span></span>


<span data-ttu-id="e8804-104">Vous pouvez utiliser une ligne de commande pour séquencer une nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="e8804-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="e8804-105">L’utilisation d’une ligne de commande est utile lorsque vous devez créer un grand nombre d’applications virtuelles ou lorsque vous avez besoin de créer des applications séquencées sur une base récurrente.</span><span class="sxs-lookup"><span data-stu-id="e8804-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="e8804-106">Important</span><span class="sxs-lookup"><span data-stu-id="e8804-106">Important</span></span>**  
<span data-ttu-id="e8804-107">Le séquençage de la ligne de commande ne peut être utilisé que pour le séquençage par défaut.</span><span class="sxs-lookup"><span data-stu-id="e8804-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="e8804-108">Si vous devez modifier les paramètres d’installation par défaut de l’application que vous séquençage, vous devez modifier manuellement l’application virtuelle ou la mettre à jour à l’aide du Sequencer Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="e8804-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="e8804-109">Pour plus d’informations sur la mise à jour d’une application virtuelle à l’aide du Sequencer App-V, voir [Comment mettre à niveau une application virtuelle existante](how-to-upgrade-an-existing-virtual-application.md).</span><span class="sxs-lookup"><span data-stu-id="e8804-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="e8804-110">Utilisez la procédure suivante pour créer une application virtuelle à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e8804-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="e8804-111">Pour séquencer une application à l’aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="e8804-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="e8804-112">Sur l’ordinateur exécutant le Sequencer App-V, ouvrez l’invite de commandes en sélectionnant **Démarrer**, **exécuter**, puis tapez **cmd**.</span><span class="sxs-lookup"><span data-stu-id="e8804-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="e8804-113">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8804-113">Click **OK**.</span></span>

2.  <span data-ttu-id="e8804-114">Utilisez l’invite de commandes pour spécifier l’emplacement où le Sequencer App-V est installé.</span><span class="sxs-lookup"><span data-stu-id="e8804-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="e8804-115">Par exemple, à l’invite de commandes, vous pouvez taper ce qui suit: **CD C:\\Program Files\\Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="e8804-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="e8804-116">À l’invite de commandes, tapez la commande suivante, en remplaçant le texte entre guillemets par vos valeurs:</span><span class="sxs-lookup"><span data-stu-id="e8804-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="e8804-117">Remarque</span><span class="sxs-lookup"><span data-stu-id="e8804-117">Note</span></span>**  
    <span data-ttu-id="e8804-118">Vous pouvez spécifier des paramètres supplémentaires à l’aide de la ligne de commande, en fonction de la complexité de l’application que vous séquençage.</span><span class="sxs-lookup"><span data-stu-id="e8804-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="e8804-119">Pour obtenir la liste complète des paramètres disponibles pour une utilisation avec le Sequencer App-V, voir [paramètres de ligne de commande du Sequencer](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e8804-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



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
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="e8804-120">Appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="e8804-120">Press **Enter**.</span></span>

## <span data-ttu-id="e8804-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8804-121">Related topics</span></span>


[<span data-ttu-id="e8804-122">Comment créer ou mettre à niveau des applications virtuelles à l’aide du Sequencer App-V</span><span class="sxs-lookup"><span data-stu-id="e8804-122">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="e8804-123">Codes des erreurs de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="e8804-123">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="e8804-124">Paramètres de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="e8804-124">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









