---
title: Procédure pour créer le répertoire racine de package
description: Procédure pour créer le répertoire racine de package
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807182"
---
# <span data-ttu-id="b6c5d-103">Procédure pour créer le répertoire racine de package</span><span class="sxs-lookup"><span data-stu-id="b6c5d-103">How to Create the Package Root Directory</span></span>


<span data-ttu-id="b6c5d-104">Le répertoire racine du package est le répertoire de l’ordinateur exécutant le Sequencer App-V dans lequel les fichiers de l’application séquencée sont installés.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-104">The package root directory is the directory on the computer running the App-V Sequencer where files for the sequenced application are installed.</span></span> <span data-ttu-id="b6c5d-105">Ce répertoire existe également virtuellement sur l’ordinateur sur lequel une application séquencée sera diffusée.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-105">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span> <span data-ttu-id="b6c5d-106">Vous devez créer le répertoire racine du package avant de surveiller l’installation d’une nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-106">You should create the package root directory before you monitor the installation of a new application.</span></span>

<span data-ttu-id="b6c5d-107">Une fois que vous avez créé le répertoire racine du package, vous pouvez commencer à Sequencer les applications.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-107">After you have created the package root directory, you can begin sequencing applications.</span></span> <span data-ttu-id="b6c5d-108">Pour plus d’informations sur le séquençage d’une nouvelle application, voir [Comment installer le Sequencer](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="b6c5d-108">For more information about sequencing a new application, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

**<span data-ttu-id="b6c5d-109">Pour créer le répertoire racine du package</span><span class="sxs-lookup"><span data-stu-id="b6c5d-109">To create the package root directory</span></span>**

1.  <span data-ttu-id="b6c5d-110">Pour créer le répertoire racine du package, sur l’ordinateur exécutant le Sequencer App-V, mappez le lecteur Q:\\ à l’emplacement réseau spécifié.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-110">To create the package root directory, on the computer running the App-V Sequencer, map the Q:\\ drive to the specified network location.</span></span> <span data-ttu-id="b6c5d-111">L’emplacement que vous spécifiez doit disposer d’un espace suffisant pour enregistrer l’application que vous séquençage.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-111">The location you specify should have sufficient space to save the application you are sequencing.</span></span>

2.  <span data-ttu-id="b6c5d-112">Pour créer un répertoire que vous pouvez utiliser pour une nouvelle application virtuelle, créez un dossier sur le lecteur Q:\\ et attribuez-lui un nom.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-112">To create a directory that you can use for a new virtual application, create a folder on the Q:\\ drive and assign it a name.</span></span>

    <span data-ttu-id="b6c5d-113">**Important**  Le nom que vous attribuez aux fichiers d’application virtuels qui seront enregistrés dans le répertoire racine du package doit utiliser le format de noms 8,3.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-113">**Important** The name you assign to virtual application files that will be saved in the package root directory should use the 8.3 naming format.</span></span> <span data-ttu-id="b6c5d-114">Les noms de fichiers ne doivent pas comporter plus de 8 caractères avec une extension de nom de fichier à trois caractères.</span><span class="sxs-lookup"><span data-stu-id="b6c5d-114">The file names should be no longer than 8 characters with a three-character file name extension.</span></span>

     

## <span data-ttu-id="b6c5d-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6c5d-115">Related topics</span></span>


[<span data-ttu-id="b6c5d-116">Tâches pour Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="b6c5d-116">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





