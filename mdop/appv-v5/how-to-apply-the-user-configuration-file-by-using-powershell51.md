---
title: Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell
description: Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell
author: dansimp
ms.assetid: 986e638c-4a0c-4a7e-be73-f4615e8b8000
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97b3db253993d6d855384ee5d9771a7f9ff5b64d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805719"
---
# <span data-ttu-id="1d752-103">Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="1d752-103">How to Apply the User Configuration File by Using PowerShell</span></span>


<span data-ttu-id="1d752-104">Le fichier de configuration utilisateur dynamique est appliqué lors de la publication d’un package pour un utilisateur spécifique et détermine la façon dont le package s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="1d752-104">The dynamic user configuration file is applied when a package is published to a specific user and determines how the package will run.</span></span>

<span data-ttu-id="1d752-105">Utilisez la procédure suivante pour spécifier un fichier de configuration spécifique à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1d752-105">Use the following procedure to specify a user-specific configuration file.</span></span> <span data-ttu-id="1d752-106">La procédure suivante est basée sur l’exemple:</span><span class="sxs-lookup"><span data-stu-id="1d752-106">The following procedure is based on the example:</span></span>

**<span data-ttu-id="1d752-107">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="1d752-107">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="1d752-108">Pour appliquer un fichier de configuration utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d752-108">To apply a user Configuration file</span></span>**

1.  <span data-ttu-id="1d752-109">Pour ajouter le package à l’ordinateur à l’aide de la console PowerShell, tapez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="1d752-109">To add the package to the computer using the PowerShell console type the following command:</span></span>

    <span data-ttu-id="1d752-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.</span><span class="sxs-lookup"><span data-stu-id="1d752-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.</span></span>

2.  <span data-ttu-id="1d752-111">Utilisez la commande suivante pour publier le package pour l’utilisateur et spécifier le fichier de configuration utilisateur dynamique mis à jour:</span><span class="sxs-lookup"><span data-stu-id="1d752-111">Use the following command to publish the package to the user and specify the updated the dynamic user configuration file:</span></span>

    **<span data-ttu-id="1d752-112">Publisher-AppVClientPackage $pkg-DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span><span class="sxs-lookup"><span data-stu-id="1d752-112">Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span></span>**

    <span data-ttu-id="1d752-113">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="1d752-113">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="1d752-114">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="1d752-114">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="1d752-115">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="1d752-115">Got an App-V issue?</span></span>** <span data-ttu-id="1d752-116">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="1d752-116">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="1d752-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d752-117">Related topics</span></span>


[<span data-ttu-id="1d752-118">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="1d752-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





