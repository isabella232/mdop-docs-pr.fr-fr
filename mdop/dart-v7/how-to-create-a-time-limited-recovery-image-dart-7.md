---
title: Procédure de création d'une image de récupération limitée dans le temps
description: Procédure de création d'une image de récupération limitée dans le temps
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804374"
---
# <span data-ttu-id="25524-103">Procédure de création d'une image de récupération limitée dans le temps</span><span class="sxs-lookup"><span data-stu-id="25524-103">How to Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="25524-104">Vous pouvez créer une image de récupération DaRT qui ne peut être utilisée que pendant un certain nombre de jours après sa génération.</span><span class="sxs-lookup"><span data-stu-id="25524-104">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="25524-105">Pour cela, vous devez exécuter l' **Assistant image de récupération DART** à une invite de commandes et spécifier le nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="25524-105">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

**<span data-ttu-id="25524-106">Pour créer une image de récupération ayant une limite de temps</span><span class="sxs-lookup"><span data-stu-id="25524-106">To create a recovery image that has a time limit</span></span>**

1.  <span data-ttu-id="25524-107">Ouvrez une invite de commandes avec des informations d’identification d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="25524-107">Open a Command Prompt with administrator credentials.</span></span>

2.  <span data-ttu-id="25524-108">Remplacez le répertoire par l’emplacement du programme ERDC.exe.</span><span class="sxs-lookup"><span data-stu-id="25524-108">Change the directory to the location of the ERDC.exe program.</span></span>

3.  <span data-ttu-id="25524-109">À l’aide de la syntaxe suivante, exécutez l' **Assistant image de récupération DART**.</span><span class="sxs-lookup"><span data-stu-id="25524-109">Using the following syntax, run the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="25524-110">*NumberOfDays* est un entier positif qui représente le nombre de jours pendant lesquels l’image de récupération DART sera utilisable.</span><span class="sxs-lookup"><span data-stu-id="25524-110">*NumberOfDays* is a positive integer that represents the number of days that the DaRT recovery image will be usable.</span></span>

    ``` syntax
    ERDC /e NumberOfDays
    ```

## <span data-ttu-id="25524-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="25524-111">Related topics</span></span>


[<span data-ttu-id="25524-112">Création de l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="25524-112">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





