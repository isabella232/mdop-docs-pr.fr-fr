---
title: Planification pour créer l'image de récupération DaRT8.0
description: Planification pour créer l'image de récupération DaRT8.0
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810776"
---
# <span data-ttu-id="d0d0c-103">Planification pour créer l'image de récupération DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="d0d0c-103">Planning to Create the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="d0d0c-104">Utilisez les informations fournies dans cette section lorsque vous envisagez de créer l’image de récupération du jeu d’outils de diagnostics et de récupération Microsoft (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

## <span data-ttu-id="d0d0c-105">Planification de la création de l’image de récupération 8,0 de DaRT</span><span class="sxs-lookup"><span data-stu-id="d0d0c-105">Planning to create the DaRT 8.0 recovery image</span></span>


<span data-ttu-id="d0d0c-106">Lorsque vous créez l’image de récupération DaRT, vous devez choisir les outils à inclure dans l’image.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="d0d0c-107">Pour prendre la décision, tenez compte du fait que les utilisateurs finaux peuvent avoir accès à ces outils.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="d0d0c-108">Si les techniciens du support technique emportent le média d’image de récupération aux ordinateurs des utilisateurs finaux pour diagnostiquer les problèmes, vous pouvez installer tous les outils sur l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="d0d0c-109">Si vous envisagez de diagnostiquer les ordinateurs des utilisateurs finaux à distance, vous souhaiterez peut-être désactiver certains outils, tels que l’effacement de disque et l’éditeur du Registre, puis activer d’autres outils, y compris la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="d0d0c-110">Lorsque vous créez l’image de récupération DaRT, vous devez également indiquer si vous souhaitez inclure d’autres pilotes ou fichiers.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="d0d0c-111">Déterminez les emplacements des pilotes ou fichiers supplémentaires que vous voulez inclure dans l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="d0d0c-112">Pour plus d’informations sur les outils DaRT, voir [vue d’ensemble des outils dans dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="d0d0c-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span> <span data-ttu-id="d0d0c-113">Pour plus d’informations sur la création d’une image de récupération sécurisée, voir [considérations relatives à la sécurité de DaRT 8,0](security-considerations-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="d0d0c-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 8.0](security-considerations-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="d0d0c-114">Conditions préalables à l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="d0d0c-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="d0d0c-115">Les éléments suivants sont requis ou recommandés pour la création de l’image de récupération DaRT:</span><span class="sxs-lookup"><span data-stu-id="d0d0c-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d0d0c-116">Prérequises</span><span class="sxs-lookup"><span data-stu-id="d0d0c-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="d0d0c-117">Détails</span><span class="sxs-lookup"><span data-stu-id="d0d0c-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0d0c-118">Fichiers sources de Windows 8</span><span class="sxs-lookup"><span data-stu-id="d0d0c-118">Windows 8 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0d0c-119">Requis pour créer l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="d0d0c-120">Spécifiez le chemin d’accès d’un DVD Windows 8 ou d’un fichier source Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-120">Provide the path of a Windows 8 DVD or of Windows 8 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0d0c-121">Outils de débogage Windows pour votre plate-forme</span><span class="sxs-lookup"><span data-stu-id="d0d0c-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0d0c-122">Requis lors de l’exécution <strong> de l’analyseur </strong> d’incidents pour déterminer la cause de l’échec de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="d0d0c-123">Nous vous recommandons de spécifier le chemin d’accès des outils de débogage Windows au moment de la création de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="d0d0c-124">Vous pouvez télécharger les outils de débogage Windows suivants: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> Télécharger et installer les outils de débogage pour Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="d0d0c-124">You can download the Windows Debugging Tools here: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0d0c-125">Facultatif: <strong> définitions de protection </strong></span><span class="sxs-lookup"><span data-stu-id="d0d0c-125">Optional: <strong>Defender</strong> definitions</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0d0c-126">Les définitions les plus récentes pour <strong> Defender </strong> sont nécessaires lorsque vous exécutez <strong> Defender </strong> .</span><span class="sxs-lookup"><span data-stu-id="d0d0c-126">The latest definitions for <strong>Defender</strong> are required when you run <strong>Defender</strong>.</span></span> <span data-ttu-id="d0d0c-127">Même si vous pouvez télécharger les définitions lors de l’exécution de l' <strong> </strong> outil de protection, nous vous conseillons de télécharger les dernières définitions lors de la création de l’image de récupération DART pour pouvoir continuer à exécuter l’outil avec les définitions les plus récentes, même si le problème n’est pas lié à la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-127">Although you can download the definitions when you run <strong>Defender</strong>, we recommend that you download the latest definitions at the time you create the DaRT recovery image so that you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0d0c-128">Facultatif: fichiers de symboles Windows à utiliser avec l' <strong> analyseur d’incidents</span><span class="sxs-lookup"><span data-stu-id="d0d0c-128">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d0d0c-129">En général, les informations de débogage sont stockées dans un fichier de symboles différent du programme.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-129">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="d0d0c-130">Vous devez avoir accès aux informations de symbole lors du débogage d’une application qui a cessé de répondre (par exemple, si elle a cessé de fonctionner).</span><span class="sxs-lookup"><span data-stu-id="d0d0c-130">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="d0d0c-131">Pour plus d’informations, reportez-vous à la rubrique <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> diagnostic des pannes système avec l’analyseur d’incidents </a> .</span><span class="sxs-lookup"><span data-stu-id="d0d0c-131">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d0d0c-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0d0c-132">Related topics</span></span>


[<span data-ttu-id="d0d0c-133">Planification du déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="d0d0c-133">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





