---
title: Planification pour créer l'image de récupération DaRT7.0
description: Planification pour créer l'image de récupération DaRT7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808693"
---
# <span data-ttu-id="6fe1a-103">Planification pour créer l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="6fe1a-103">Planning to Create the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="6fe1a-104">Utilisez les informations fournies dans cette section lorsque vous planifiez la création de l’image de récupération du jeu d’outils de diagnostics et de récupération Microsoft (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-104">Use the information in this section when you plan for creating the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="6fe1a-105">Planification de la création de l’image de récupération de DaRT 7</span><span class="sxs-lookup"><span data-stu-id="6fe1a-105">Planning to Create the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="6fe1a-106">Lorsque vous créez l’image de récupération DaRT, vous devez choisir les outils à inclure dans l’image.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="6fe1a-107">Lorsque vous prenez cette décision, rappelez-vous que les utilisateurs finaux peuvent avoir accès occasionnellement aux différents outils DaRT.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-107">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="6fe1a-108">Pour plus d’informations sur les outils DaRT, voir [vue d’ensemble des outils dans dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="6fe1a-108">For more information about the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span> <span data-ttu-id="6fe1a-109">Pour plus d’informations sur la création d’une image de récupération sécurisée, voir [considérations relatives à la sécurité de DaRT 7,0](security-considerations-for-dart-70-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="6fe1a-109">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 7.0](security-considerations-for-dart-70-dart-7.md).</span></span>

<span data-ttu-id="6fe1a-110">Lorsque vous créez l’image de récupération DaRT, vous devez également indiquer si vous souhaitez inclure d’autres pilotes ou fichiers.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="6fe1a-111">Déterminez les emplacements des pilotes ou fichiers supplémentaires que vous voulez inclure dans l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

## <span data-ttu-id="6fe1a-112">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="6fe1a-112">Prerequisites</span></span>


<span data-ttu-id="6fe1a-113">Les éléments suivants sont requis ou recommandés pour la création de l’image de récupération DaRT:</span><span class="sxs-lookup"><span data-stu-id="6fe1a-113">The following items are required or recommended for creating the DaRT recovery image:</span></span>

-   <span data-ttu-id="6fe1a-114">Fichiers sources de Windows 7</span><span class="sxs-lookup"><span data-stu-id="6fe1a-114">Windows 7 source files</span></span>

    <span data-ttu-id="6fe1a-115">Vous devez indiquer le chemin d’accès d’un DVD Windows 7 ou d’un fichier source Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-115">You must provide the path of a Windows 7 DVD or of Windows 7 source files.</span></span> <span data-ttu-id="6fe1a-116">Les fichiers sources de Windows 7 sont requis pour créer l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-116">Windows 7 source files are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="6fe1a-117">Outils de débogage Windows pour votre plate-forme</span><span class="sxs-lookup"><span data-stu-id="6fe1a-117">Windows Debugging Tools for your platform</span></span>

    <span data-ttu-id="6fe1a-118">Les outils de débogage de Windows sont requis lorsque vous exécutez l' **analyseur d’incidents** pour déterminer la cause du blocage sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-118">Windows Debugging Tools are required when you run **Crash Analyzer** to determine the cause of a computer crash.</span></span> <span data-ttu-id="6fe1a-119">Nous vous recommandons de spécifier le chemin d’accès des outils de débogage Windows au moment de la création de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-119">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="6fe1a-120">Le cas échéant, vous pouvez télécharger les outils de débogage Windows suivants: [Télécharger et installer les outils de débogage pour Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="6fe1a-120">If it is necessary, you can download the Windows Debugging Tools here: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

-   <span data-ttu-id="6fe1a-121">Facultatif: définitions des **nettoyeurs de systèmes autonomes**</span><span class="sxs-lookup"><span data-stu-id="6fe1a-121">Optional: **Standalone System Sweeper** definitions</span></span>

    <span data-ttu-id="6fe1a-122">Les définitions les plus récentes pour le **nettoyeur système autonome** sont nécessaires lorsque vous exécutez cet outil.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-122">The latest definitions for the **Standalone System Sweeper** are required when you run this tool.</span></span> <span data-ttu-id="6fe1a-123">Même si vous pouvez télécharger les définitions lors de l’exécution du **nettoyeur de systèmes autonome**, nous vous recommandons de télécharger les définitions les plus récentes au moment où vous créez l’image de récupération Dart.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-123">Although you can download the definitions when you run **Standalone System Sweeper**, we recommend that you download the latest definitions at the time you create the DaRT recovery image.</span></span> <span data-ttu-id="6fe1a-124">De cette manière, vous pouvez toujours exécuter l’outil avec les définitions les plus récentes même si le problème ne se connecte pas à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-124">In this manner, you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span>

-   <span data-ttu-id="6fe1a-125">Facultatif: fichiers de symboles Windows à utiliser avec l' **analyseur d’incidents**</span><span class="sxs-lookup"><span data-stu-id="6fe1a-125">Optional: Windows symbols files for use with **Crash Analyzer**</span></span>

    <span data-ttu-id="6fe1a-126">En général, les informations de débogage sont stockées dans un fichier de symboles différent du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="6fe1a-126">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="6fe1a-127">Vous devez avoir accès aux informations de symbole lors du débogage d’une application qui a cessé de répondre (par exemple, si elle a été bloquée).</span><span class="sxs-lookup"><span data-stu-id="6fe1a-127">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span> <span data-ttu-id="6fe1a-128">Pour plus d’informations, reportez-vous à la rubrique [diagnostic des pannes système avec l’analyseur d’incidents](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="6fe1a-128">For more information, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span></span>

## <span data-ttu-id="6fe1a-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6fe1a-129">Related topics</span></span>


[<span data-ttu-id="6fe1a-130">Planification du déploiement de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="6fe1a-130">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





