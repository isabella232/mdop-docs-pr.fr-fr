---
title: Planification pour créer l'image de récupération DaRT10
description: Planification pour créer l'image de récupération DaRT10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809678"
---
# <span data-ttu-id="911d3-103">Planification pour créer l'image de récupération DaRT10</span><span class="sxs-lookup"><span data-stu-id="911d3-103">Planning to Create the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="911d3-104">Utilisez les informations de cette section lorsque vous envisagez de créer l’image de récupération Microsoft Diagnostics and Recovery Tools (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="911d3-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

## <span data-ttu-id="911d3-105">Planification de la création de l’image de récupération de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="911d3-105">Planning to create the DaRT 10 recovery image</span></span>


<span data-ttu-id="911d3-106">Lorsque vous créez l’image de récupération DaRT, vous devez choisir les outils à inclure dans l’image.</span><span class="sxs-lookup"><span data-stu-id="911d3-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="911d3-107">Pour prendre la décision, tenez compte du fait que les utilisateurs finaux peuvent avoir accès à ces outils.</span><span class="sxs-lookup"><span data-stu-id="911d3-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="911d3-108">Si les techniciens du support technique emportent le média d’image de récupération aux ordinateurs des utilisateurs finaux pour diagnostiquer les problèmes, vous pouvez installer tous les outils sur l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="911d3-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="911d3-109">Si vous envisagez de diagnostiquer les ordinateurs des utilisateurs finaux à distance, vous souhaiterez peut-être désactiver certains outils, tels que l’effacement de disque et l’éditeur du Registre, puis activer d’autres outils, y compris la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="911d3-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="911d3-110">Lorsque vous créez l’image de récupération DaRT, vous devez également indiquer si vous souhaitez inclure d’autres pilotes ou fichiers.</span><span class="sxs-lookup"><span data-stu-id="911d3-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="911d3-111">Déterminez les emplacements des pilotes ou fichiers supplémentaires que vous voulez inclure dans l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="911d3-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="911d3-112">Pour plus d’informations sur les outils DaRT, voir [vue d’ensemble des outils dans DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="911d3-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span> <span data-ttu-id="911d3-113">Pour plus d’informations sur la création d’une image de récupération sécurisée, voir [considérations relatives à la sécurité de DART 10](security-considerations-for-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="911d3-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 10](security-considerations-for-dart-10.md).</span></span>

## <span data-ttu-id="911d3-114">Conditions préalables à l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="911d3-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="911d3-115">Les éléments suivants sont requis ou recommandés pour la création de l’image de récupération DaRT:</span><span class="sxs-lookup"><span data-stu-id="911d3-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="911d3-116">Prérequises</span><span class="sxs-lookup"><span data-stu-id="911d3-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="911d3-117">Détails</span><span class="sxs-lookup"><span data-stu-id="911d3-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="911d3-118">Fichiers sources Windows 10</span><span class="sxs-lookup"><span data-stu-id="911d3-118">Windows 10 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="911d3-119">Requis pour créer l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="911d3-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="911d3-120">Spécifiez le chemin d’accès d’un DVD Windows 10 ou d’un fichier source Windows 10.</span><span class="sxs-lookup"><span data-stu-id="911d3-120">Provide the path of a Windows 10 DVD or of Windows 10 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="911d3-121">Outils de débogage Windows pour votre plate-forme</span><span class="sxs-lookup"><span data-stu-id="911d3-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="911d3-122">Requis lors de l’exécution <strong> de l’analyseur </strong> d’incidents pour déterminer la cause de l’échec de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="911d3-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="911d3-123">Nous vous recommandons de spécifier le chemin d’accès des outils de débogage Windows au moment de la création de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="911d3-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="911d3-124">Vous pouvez télécharger les outils de débogage Windows suivants: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> Télécharger et installer les outils de débogage pour Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="911d3-124">You can download the Windows Debugging Tools here: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="911d3-125">Facultatif: fichiers de symboles Windows à utiliser avec l' <strong> analyseur d’incidents</span><span class="sxs-lookup"><span data-stu-id="911d3-125">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="911d3-126">En général, les informations de débogage sont stockées dans un fichier de symboles différent du programme.</span><span class="sxs-lookup"><span data-stu-id="911d3-126">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="911d3-127">Vous devez avoir accès aux informations de symbole lors du débogage d’une application qui a cessé de répondre (par exemple, si elle a cessé de fonctionner).</span><span class="sxs-lookup"><span data-stu-id="911d3-127">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="911d3-128">Pour plus d’informations, reportez-vous à la rubrique <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> diagnostic des pannes système avec l’analyseur d’incidents </a> .</span><span class="sxs-lookup"><span data-stu-id="911d3-128">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="911d3-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="911d3-129">Related topics</span></span>

[<span data-ttu-id="911d3-130">Planification du déploiement de DaRT10</span><span class="sxs-lookup"><span data-stu-id="911d3-130">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 




