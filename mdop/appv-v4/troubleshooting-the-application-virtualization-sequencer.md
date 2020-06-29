---
title: Résolution des problèmes liés à Application Virtualization Sequencer
description: Résolution des problèmes liés à Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806205"
---
# <span data-ttu-id="2b82b-103">Résolution des problèmes liés à Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2b82b-103">Troubleshooting the Application Virtualization Sequencer</span></span>


<span data-ttu-id="2b82b-104">Cette rubrique contient des informations que vous pouvez utiliser pour résoudre les problèmes d’ordre général sur le Sequencer Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="2b82b-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="2b82b-105">La création d’un fichier SFTD à l’aide du Sequencer App-V augmente le numéro de version de manière inattendue</span><span class="sxs-lookup"><span data-stu-id="2b82b-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="2b82b-106">Le numéro de version associé à un fichier SFTD augmente de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="2b82b-106">The version number associated with an SFTD file increases unexpectedly.</span></span>

**<span data-ttu-id="2b82b-107">Solution</span><span class="sxs-lookup"><span data-stu-id="2b82b-107">Solution</span></span>**

<span data-ttu-id="2b82b-108">Utilisez la ligne de commande pour générer un nouveau fichier. sft.</span><span class="sxs-lookup"><span data-stu-id="2b82b-108">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="2b82b-109">Pour créer le fichier. SFT à l’aide de la ligne de commande, entrez ce qui suit à l’invite de commandes:</span><span class="sxs-lookup"><span data-stu-id="2b82b-109">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="2b82b-110">mkdiffpkg.exe &lt; nom de fichier SFT de base &gt; &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="2b82b-110">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="2b82b-111">Le nom de fichier du fichier OSD n’est pas correct après la mise à niveau du package</span><span class="sxs-lookup"><span data-stu-id="2b82b-111">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="2b82b-112">Après avoir effectué la mise à niveau d’un package existant, le nom du fichier n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="2b82b-112">After you upgrade an existing package, the file name is not correct.</span></span>

**<span data-ttu-id="2b82b-113">Solution</span><span class="sxs-lookup"><span data-stu-id="2b82b-113">Solution</span></span>**

<span data-ttu-id="2b82b-114">Lorsque vous ouvrez un package pour la mise à niveau, vous devez spécifier le lecteur Q:\\ racine en tant qu’emplacement de sortie du package.</span><span class="sxs-lookup"><span data-stu-id="2b82b-114">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="2b82b-115">Ne spécifiez pas un nom de fichier associé avec l’emplacement de sortie.</span><span class="sxs-lookup"><span data-stu-id="2b82b-115">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="2b82b-116">L’installation par défaut de Microsoft Word2003 génère une erreur lors d’un flux vers un client</span><span class="sxs-lookup"><span data-stu-id="2b82b-116">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="2b82b-117">Lorsque vous diffusez en continu Microsoft Word2003 sur un client, une erreur est retournée, mais Microsoft Word continue de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="2b82b-117">When you stream Microsoft Word2003 to a client, an error is returned but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="2b82b-118">Solution</span><span class="sxs-lookup"><span data-stu-id="2b82b-118">Solution</span></span>**

<span data-ttu-id="2b82b-119">Reséquencez le package d’application virtuel, puis sélectionnez **installation complète**.</span><span class="sxs-lookup"><span data-stu-id="2b82b-119">Resequence the virtual application package, and select **Full Install**.</span></span>

## <span data-ttu-id="2b82b-120">La mise à niveau du package ne fonctionne pas lorsque vous créez un package dépendant</span><span class="sxs-lookup"><span data-stu-id="2b82b-120">Package Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="2b82b-121">Lorsque vous créez un package dépendant en utilisant la mise à niveau du package et en ajoutant de nouvelles entrées de Registre, il semble fonctionner correctement, mais les entrées de Registre mises à jour ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="2b82b-121">When you create a dependent package by using package upgrade and add new registry entries, it appears to function correctly but the updated registry entries are not available.</span></span>

**<span data-ttu-id="2b82b-122">Solution</span><span class="sxs-lookup"><span data-stu-id="2b82b-122">Solution</span></span>**

<span data-ttu-id="2b82b-123">Les paramètres de Registre étant toujours stockés avec la version d’origine du package, les mises à jour apportées au package ne semblent pas être disponibles sauf si vous réparez le package d’origine.</span><span class="sxs-lookup"><span data-stu-id="2b82b-123">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="2b82b-124">Erreur lors de la tentative de séquence. .NET 2.0</span><span class="sxs-lookup"><span data-stu-id="2b82b-124">Error When Trying to Sequence .NET2.0</span></span>


<span data-ttu-id="2b82b-125">Lorsque vous séquencez un package qui nécessite. .NET 2.0 vous obtenez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2b82b-125">When you sequence a package that requires .NET2.0, you get an error.</span></span>

**<span data-ttu-id="2b82b-126">Solution</span><span class="sxs-lookup"><span data-stu-id="2b82b-126">Solution</span></span>**

<span data-ttu-id="2b82b-127">Séquençage des packages qui nécessitent. NET 2.0 n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2b82b-127">Sequencing packages that require .NET2.0 is not supported.</span></span>

## <span data-ttu-id="2b82b-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b82b-128">Related topics</span></span>


[<span data-ttu-id="2b82b-129">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2b82b-129">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





