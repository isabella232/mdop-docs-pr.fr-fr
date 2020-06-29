---
title: Résolution des problèmes liés à Application Virtualization Sequencer
description: Résolution des problèmes liés à Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806229"
---
# <span data-ttu-id="af310-103">Résolution des problèmes liés à Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="af310-103">Troubleshooting Application Virtualization Sequencer Issues</span></span>


<span data-ttu-id="af310-104">Cette rubrique contient des informations que vous pouvez utiliser pour résoudre les problèmes d’ordre général sur le Sequencer Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="af310-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="af310-105">La création d’un fichier SFTD à l’aide du Sequencer App-V augmente le numéro de version de manière inattendue</span><span class="sxs-lookup"><span data-stu-id="af310-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="af310-106">Utilisez la ligne de commande pour générer un nouveau fichier. sft.</span><span class="sxs-lookup"><span data-stu-id="af310-106">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="af310-107">Pour créer le fichier. SFT à l’aide de la ligne de commande, entrez ce qui suit à l’invite de commandes:</span><span class="sxs-lookup"><span data-stu-id="af310-107">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="af310-108">mkdiffpkg.exe &lt; nom de fichier SFT de base &gt; &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="af310-108">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="af310-109">Le nom de fichier du fichier OSD n’est pas correct après la mise à niveau du package</span><span class="sxs-lookup"><span data-stu-id="af310-109">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="af310-110">Lorsque vous ouvrez un package pour la mise à niveau, vous devez spécifier le lecteur Q:\\ racine en tant qu’emplacement de sortie du package.</span><span class="sxs-lookup"><span data-stu-id="af310-110">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="af310-111">Ne spécifiez pas un nom de fichier associé avec l’emplacement de sortie.</span><span class="sxs-lookup"><span data-stu-id="af310-111">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="af310-112">L’installation par défaut de Microsoft Word2003 génère une erreur lors d’un flux vers un client</span><span class="sxs-lookup"><span data-stu-id="af310-112">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="af310-113">Lorsque vous diffusez en continu Microsoft Word2003 sur un client, une erreur est retournée, mais Microsoft Word continue de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="af310-113">When you stream Microsoft Word2003 to a client, an error is returned, but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="af310-114">Solution</span><span class="sxs-lookup"><span data-stu-id="af310-114">Solution</span></span>**

<span data-ttu-id="af310-115">Reséquencez le package d’application virtuel et sélectionnez **installation complète**.</span><span class="sxs-lookup"><span data-stu-id="af310-115">Resequence the virtual application package and select **Full Install**.</span></span>

## <span data-ttu-id="af310-116">La mise à niveau active ne fonctionne pas lors de la création d’un package dépendant</span><span class="sxs-lookup"><span data-stu-id="af310-116">Active Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="af310-117">Lorsque vous créez un package dépendant en utilisant la mise à niveau active et en ajoutant de nouvelles entrées de Registre, ce dernier semble fonctionner correctement, mais les entrées de Registre mises à jour ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="af310-117">When you create a dependent package by using active upgrade and add new registry entries, it appears to function correctly, but the updated registry entries are not available.</span></span>

**<span data-ttu-id="af310-118">Solution</span><span class="sxs-lookup"><span data-stu-id="af310-118">Solution</span></span>**

<span data-ttu-id="af310-119">Les paramètres de Registre étant toujours stockés avec la version d’origine du package, les mises à jour apportées au package ne semblent pas être disponibles sauf si vous réparez le package d’origine.</span><span class="sxs-lookup"><span data-stu-id="af310-119">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="af310-120">Les informations détaillées ne sont pas visibles pour les documents Microsoft Office2007 à l’aide de la page de propriétés</span><span class="sxs-lookup"><span data-stu-id="af310-120">Detailed information is not visible for Microsoft Office2007 documents by using the properties page</span></span>


<span data-ttu-id="af310-121">Lorsque vous essayez d’afficher des informations détaillées associées à un document Microsoft Office2007 à l’aide de la page de propriétés, les informations détaillées ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="af310-121">When you try to view detailed information associated with a Microsoft Office2007 document by using the properties page, the detailed information is not visible.</span></span>

**<span data-ttu-id="af310-122">Solution</span><span class="sxs-lookup"><span data-stu-id="af310-122">Solution</span></span>**

<span data-ttu-id="af310-123">App-V ne prend pas en charge les extensions d’environnement requises pour ces pages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="af310-123">App-V does not support the required shell extensions for these property pages.</span></span>

## <span data-ttu-id="af310-124">Certaines clés de registre ne sont pas capturées lors de la séquence des applications 16 bits</span><span class="sxs-lookup"><span data-stu-id="af310-124">Some registry keys are not captured when you sequence 16-bit applications</span></span>


<span data-ttu-id="af310-125">Dans App-V 4,5, le raccordement du registre a été déplacé du mode noyau au mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="af310-125">In App-V 4.5, registry hooking has been moved from kernel mode to user mode.</span></span> <span data-ttu-id="af310-126">Si vous souhaitez séquencer une application 16 bits ou une application qui utilise un programme d’installation 16 bits, vous devez commencer par configurer l’ordinateur Sequencer de manière à ce que le processus s’exécute dans sa propre copie de la machine DOS virtuelle Windows NT (NTVDM).</span><span class="sxs-lookup"><span data-stu-id="af310-126">If you want to sequence a 16-bit application or an application that uses a 16-bit installer, you must first configure the sequencer computer so that the process runs in its own copy of the Windows NT Virtual DOS Machine (NTVDM).</span></span>

**<span data-ttu-id="af310-127">Solution</span><span class="sxs-lookup"><span data-stu-id="af310-127">Solution</span></span>**

<span data-ttu-id="af310-128">Avant de séquencer l’application, définissez la valeur de clé de Registre REGSZ globale suivante sur «Yes» sur l’ordinateur de séquençage:</span><span class="sxs-lookup"><span data-stu-id="af310-128">Before you sequence the application, set the following global REGSZ registry key value to "yes" on the sequencing computer:</span></span>

<span data-ttu-id="af310-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span><span class="sxs-lookup"><span data-stu-id="af310-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span></span>

<span data-ttu-id="af310-130">Vous devez redémarrer votre ordinateur pour que cette action soit prise en compte.</span><span class="sxs-lookup"><span data-stu-id="af310-130">You must restart the computer before this takes effect.</span></span>

## <span data-ttu-id="af310-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af310-131">Related topics</span></span>


[<span data-ttu-id="af310-132">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="af310-132">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





