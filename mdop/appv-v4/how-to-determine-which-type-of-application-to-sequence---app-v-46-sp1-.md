---
title: Déterminer le type d’application à séquence (App-V 4,6 SP1)
description: Déterminer le type d’application à séquence (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807126"
---
# <span data-ttu-id="b3579-103">Déterminer le type d’application à séquence (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="b3579-103">How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)</span></span>


<span data-ttu-id="b3579-104">Vous pouvez séquencer trois types d’applications de base à l’aide du Sequencer Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="b3579-104">You can sequence three basic types of applications by using Microsoft Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="b3579-105">Pour déterminer le type d’application à séquencer</span><span class="sxs-lookup"><span data-stu-id="b3579-105">To determine which type of application to sequence</span></span>


<span data-ttu-id="b3579-106">Utilisez le tableau suivant pour déterminer le type d’application que vous devez séquencer et obtenir plus d’informations sur la façon de séquencer l’application.</span><span class="sxs-lookup"><span data-stu-id="b3579-106">Use the following table to determine which type of application you should sequence and to obtain more information about how to sequence the application.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b3579-107">Type d’application</span><span class="sxs-lookup"><span data-stu-id="b3579-107">Application Type</span></span></th>
<th align="left"><span data-ttu-id="b3579-108">Description</span><span class="sxs-lookup"><span data-stu-id="b3579-108">Description</span></span></th>
<th align="left"><span data-ttu-id="b3579-109">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b3579-109">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3579-110">Standard</span><span class="sxs-lookup"><span data-stu-id="b3579-110">Standard</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3579-111">Sélectionnez cette option pour créer un package qui contient une application ou une suite d’applications.</span><span class="sxs-lookup"><span data-stu-id="b3579-111">Select this option to create a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="b3579-112">Cette option doit être sélectionnée pour la plupart des applications que vous envisagez de séquencer.</span><span class="sxs-lookup"><span data-stu-id="b3579-112">You should select this option for most applications that you plan to sequence.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)"><span data-ttu-id="b3579-113">Procédure pour séquencer une nouvelle application standard (App-V4.6SP1</span><span class="sxs-lookup"><span data-stu-id="b3579-113">How to Sequence a New Standard Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b3579-114">Module complémentaire ou plug-in</span><span class="sxs-lookup"><span data-stu-id="b3579-114">Add-on or Plug-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3579-115">Sélectionnez cette option pour créer un package qui étend les fonctionnalités d’une application standard, par exemple un plug-in pour Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b3579-115">Select this option to create a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="b3579-116">De plus, vous pouvez utiliser les plug-ins pour les applications installées en mode natif ou un autre package lié à l’aide de la composition suite dynamique.</span><span class="sxs-lookup"><span data-stu-id="b3579-116">Additionally, you can use plug-ins for natively installed applications, or another package that is linked by using Dynamic Suite Composition.</span></span> <span data-ttu-id="b3579-117">Pour plus d’informations sur la composition de la suite dynamique, voir <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> utilisation de la composition suite dynamique </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="b3579-117">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)"><span data-ttu-id="b3579-118">Procédure pour séquencer un nouveau module complémentaire ou plug-in (App-V4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="b3579-118">How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b3579-119">Intergiciels</span><span class="sxs-lookup"><span data-stu-id="b3579-119">Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="b3579-120">Sélectionnez cette option pour créer un package requis par une application standard (par exemple, Microsoft .NET Framework).</span><span class="sxs-lookup"><span data-stu-id="b3579-120">Select this option to create a package that is required by a standard application, for example, the Microsoft .NET Framework.</span></span> <span data-ttu-id="b3579-121">Les packages middleware permettent de créer des liens vers d’autres packages à l’aide de la composition suite dynamique.</span><span class="sxs-lookup"><span data-stu-id="b3579-121">Middleware packages are used for linking to other packages by using Dynamic Suite Composition.</span></span> <span data-ttu-id="b3579-122">Pour plus d’informations sur la composition de la suite dynamique, voir <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> utilisation de la composition suite dynamique </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="b3579-122">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)"><span data-ttu-id="b3579-123">Procédure pour séquencer une nouvelle application d'intergiciel (middleware) (App-V4.6SP1)</span><span class="sxs-lookup"><span data-stu-id="b3579-123">How to Sequence a New Middleware Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b3579-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3579-124">Related topics</span></span>


[<span data-ttu-id="b3579-125">Tâches pour Application Virtualization Sequencer (App-V4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="b3579-125">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





