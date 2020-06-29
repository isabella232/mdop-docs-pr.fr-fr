---
title: Comment convertir un package créé dans une version précédente d'App-V
description: Comment convertir un package créé dans une version précédente d'App-V
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805670"
---
# <span data-ttu-id="639eb-103">Comment convertir un package créé dans une version précédente d'App-V</span><span class="sxs-lookup"><span data-stu-id="639eb-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="639eb-104">Vous pouvez utiliser l’utilitaire convertisseur de package pour mettre à niveau des packages d’application virtuels qui ont été créés dans des versions antérieures d’App-V.</span><span class="sxs-lookup"><span data-stu-id="639eb-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="639eb-105">Remarque</span><span class="sxs-lookup"><span data-stu-id="639eb-105">Note</span></span>**  
<span data-ttu-id="639eb-106">Si vous utilisez un ordinateur avec une architecture 64 bits, vous devez utiliser la version x86 de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="639eb-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="639eb-107">Le convertisseur de package peut uniquement convertir les packages qui ont été créés à l’aide du Sequencer App-V 4,5 ou d’une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="639eb-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="639eb-108">Les packages créés à l’aide d’une version antérieure à App-V 4,5 doivent être mis à niveau vers le format App-V 4,5 ou App-V 4,6 avant la conversion.</span><span class="sxs-lookup"><span data-stu-id="639eb-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="639eb-109">Les informations suivantes fournissent une direction pour la conversion des packages d’application virtuelle existants.</span><span class="sxs-lookup"><span data-stu-id="639eb-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="639eb-110">Important</span><span class="sxs-lookup"><span data-stu-id="639eb-110">Important</span></span>**  
<span data-ttu-id="639eb-111">Vous devez configurer le convertisseur de package de façon à ce qu’il enregistre toujours le fichier de composants du package dans un emplacement et un répertoire sécurisés.</span><span class="sxs-lookup"><span data-stu-id="639eb-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="639eb-112">Un emplacement sécurisé est accessible uniquement par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="639eb-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="639eb-113">Par ailleurs, lorsque vous déployez le package, vous devez enregistrer le package à un emplacement sécurisé ou vérifier qu’aucun autre utilisateur ne peut être connecté lors du processus de conversion.</span><span class="sxs-lookup"><span data-stu-id="639eb-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="639eb-114">Prise en main</span><span class="sxs-lookup"><span data-stu-id="639eb-114">Getting started</span></span>**

1.  <span data-ttu-id="639eb-115">Installez le Sequencer App-V sur un ordinateur de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="639eb-115">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="639eb-116">Pour plus d’informations sur la façon d’installer le Sequencer, voir [Comment installer le Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="639eb-116">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2. <span data-ttu-id="639eb-117">Importer le module PowerShell requis</span><span class="sxs-lookup"><span data-stu-id="639eb-117">Import the required Powershell Module</span></span>

```powershell
Import-Module AppVPkgConverter
```

3. <span data-ttu-id="639eb-118">Les applets de commande suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="639eb-118">The following cmdlets are available:</span></span>

   -   <span data-ttu-id="639eb-119">Test-AppvLegacyPackage: cette applet de contrôle est conçue pour vérifier les packages.</span><span class="sxs-lookup"><span data-stu-id="639eb-119">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="639eb-120">Il renverra des informations sur les échecs liés au package, tels que les fichiers **. SFT** manquants, une source non valide, des erreurs de fichier **. OSD** ou une version de package non valide.</span><span class="sxs-lookup"><span data-stu-id="639eb-120">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="639eb-121">Cette applet de contrôle n’analyse pas le fichier **. SFT** ou effectue une validation approfondie.</span><span class="sxs-lookup"><span data-stu-id="639eb-121">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="639eb-122">Pour plus d’informations sur les options et les fonctionnalités de base pour cette applet de cmdlet, utilisez la fonction de saisie semi-seule PowerShell `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="639eb-122">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

   -   <span data-ttu-id="639eb-123">ConvertFrom-AppvLegacyPackage: pour convertir un package existant, tapez `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="639eb-123">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="639eb-124">Dans cette commande, `c:\contentStore` représente l’emplacement du package existant et `c:\convertedPackages` est le répertoire de sortie dans lequel le fichier de package d’application virtuelle App-V 5,0 doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="639eb-124">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.0 virtual application package file will be saved.</span></span> <span data-ttu-id="639eb-125">Par défaut, si vous ne spécifiez pas de nouveau nom, le nom de l’ancien package sera utilisé pour le nom de fichier App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="639eb-125">By default, if you do not specify a new name, the old package name will be used for the App-V 5.0 filename.</span></span>

       <span data-ttu-id="639eb-126">Par ailleurs, le convertisseur de package optimise les performances des packages dans l’application-V 5,0 en définissant le package sur l’erreur de mise en flux du package App-V.</span><span class="sxs-lookup"><span data-stu-id="639eb-126">Additionally, the package converter optimizes performance of packages in App-V 5.0 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="639eb-127">C’est plus performant que le bloc de fonctionnalités principal et qu’il télécharge entièrement le package.</span><span class="sxs-lookup"><span data-stu-id="639eb-127">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="639eb-128">L’indicateur **DownloadFullPackageOnFirstLaunch** vous permet de convertir le package et de définir le package comme étant entièrement téléchargé par défaut.</span><span class="sxs-lookup"><span data-stu-id="639eb-128">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

       **<span data-ttu-id="639eb-129">Remarque</span><span class="sxs-lookup"><span data-stu-id="639eb-129">Note</span></span>**  
       <span data-ttu-id="639eb-130">Avant de spécifier le répertoire de sortie, vous devez créer le répertoire de sortie.</span><span class="sxs-lookup"><span data-stu-id="639eb-130">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="639eb-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="639eb-131">Related topics</span></span>


[<span data-ttu-id="639eb-132">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="639eb-132">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









