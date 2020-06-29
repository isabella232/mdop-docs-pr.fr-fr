---
title: Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell
description: Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805730"
---
# <span data-ttu-id="ad24f-103">Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="ad24f-103">How to Apply the Deployment Configuration File by Using PowerShell</span></span>


<span data-ttu-id="ad24f-104">Le fichier de configuration de déploiement dynamique est appliqué lors de l’ajout ou de la définition d’un package ou d’un ordinateur exécutant le client App-V 5,1 avant la publication du package.</span><span class="sxs-lookup"><span data-stu-id="ad24f-104">The dynamic deployment configuration file is applied when a package is added or set to a computer running the App-V 5.1 client before the package has been published.</span></span> <span data-ttu-id="ad24f-105">Le fichier configure les paramètres par défaut du package pour tous les utilisateurs sur l’ordinateur exécutant le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="ad24f-105">The file configures the default settings for package for all users on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="ad24f-106">Cette section décrit les étapes utilisées pour utiliser un fichier de configuration de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ad24f-106">This section describes the steps used to use a deployment configuration file.</span></span> <span data-ttu-id="ad24f-107">La procédure est basée sur l’exemple suivant et suppose que les fichiers de package et de configuration suivants existent sur un ordinateur:</span><span class="sxs-lookup"><span data-stu-id="ad24f-107">The procedure is based on the following example and assumes the following package and configuration files exist on a computer:</span></span>

**<span data-ttu-id="ad24f-108">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="ad24f-108">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="ad24f-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="ad24f-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

**<span data-ttu-id="ad24f-110">Pour appliquer le fichier de configuration de déploiement à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="ad24f-110">To Apply the Deployment Configuration File Using PowerShell</span></span>**

-   <span data-ttu-id="ad24f-111">Pour spécifier un nouvel ensemble de configurations par défaut pour tous les utilisateurs qui exécutent le package sur un ordinateur en particulier, à l’aide d’une console PowerShell, tapez les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ad24f-111">To specify a new default set of configurations for all users who will run the package on a specific computer, using a PowerShell console type the following:</span></span>

    **<span data-ttu-id="ad24f-112">Add-AppVClientPackage-path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="ad24f-112">Add-AppVClientPackage –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

    **<span data-ttu-id="ad24f-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="ad24f-113">Note</span></span>**  
    <span data-ttu-id="ad24f-114">Cette commande capture l’objet obtenu dans $pkg.</span><span class="sxs-lookup"><span data-stu-id="ad24f-114">This command captures the resulting object into $pkg.</span></span> <span data-ttu-id="ad24f-115">Si le package est déjà présent sur l’ordinateur, vous pouvez utiliser l’applet de demande **Set-AppVclientPackage** pour appliquer le document de configuration de déploiement:</span><span class="sxs-lookup"><span data-stu-id="ad24f-115">If the package is already present on the computer, the **Set-AppVclientPackage** cmdlet can be used to apply the deployment configuration document:</span></span>

    **<span data-ttu-id="ad24f-116">Set-AppVClientPackage-nom MonApp-chemin c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="ad24f-116">Set-AppVClientPackage –Name Myapp –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="ad24f-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad24f-117">Related topics</span></span>


[<span data-ttu-id="ad24f-118">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="ad24f-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









