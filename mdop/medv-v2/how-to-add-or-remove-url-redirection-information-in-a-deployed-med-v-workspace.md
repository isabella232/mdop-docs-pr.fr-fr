---
title: Comment ajouter ou supprimer des informations de redirection des URL dans un espace de travail MED-V déployé
description: Comment ajouter ou supprimer des informations de redirection des URL dans un espace de travail MED-V déployé
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811759"
---
# <span data-ttu-id="8e9c8-103">Comment ajouter ou supprimer des informations de redirection des URL dans un espace de travail MED-V déployé</span><span class="sxs-lookup"><span data-stu-id="8e9c8-103">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>


<span data-ttu-id="8e9c8-104">Pour modifier les informations de redirection d’URL dans un espace de travail MED-V, nous vous recommandons de mettre à jour le Registre du système à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-104">To edit URL redirection information in a deployed MED-V workspace, we recommend that you update the system registry by using Group Policy.</span></span> <span data-ttu-id="8e9c8-105">Même si ce n’est pas le cas, vous pouvez également recréer et redéployer l’espace de travail MED-V avec les informations de redirection d’URL mises à jour.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-105">Although we do not recommend it, you can also rebuild and redeploy the MED-V workspace with the updated URL redirection information.</span></span>

<span data-ttu-id="8e9c8-106">La clé de Registre se trouve généralement sur:</span><span class="sxs-lookup"><span data-stu-id="8e9c8-106">The registry key is usually located at:</span></span>

<span data-ttu-id="8e9c8-107">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="8e9c8-107">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="8e9c8-108">La valeur de chaîne multiple suivante doit être présente:</span><span class="sxs-lookup"><span data-stu-id="8e9c8-108">The following multi-string value must be present:</span></span> `RedirectUrls`

<span data-ttu-id="8e9c8-109">Le champ données de la valeur pour `RedirectUrls` est une liste de l’ensemble des URL que vous avez spécifiées pour la redirection lors de la création du package d’espace de travail MED-v à l’aide du **Gestionnaire de package med-v**.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-109">The value data for `RedirectUrls` is a list of all of the URLs that you specified for redirection when you built the MED-V workspace package by using the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="8e9c8-110">Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="8e9c8-110">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="8e9c8-111">Vous pouvez ajouter et supprimer des informations de redirection d’URL en effectuant l’une des tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="8e9c8-111">You can add and remove URL redirection information by performing one of the following tasks:</span></span>

-   [<span data-ttu-id="8e9c8-112">Modifier la clé de registre de redirection d’URL et procéder au déploiement à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8e9c8-112">Edit the URL Redirection Registry Key and Deploy Using Group Policy</span></span>](#bkmk-editreg)

-   [<span data-ttu-id="8e9c8-113">Modifier le fichier texte de redirection d’URL et reconstruire l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="8e9c8-113">Edit the URL Redirection Text File and Rebuild the MED-V Workspace</span></span>](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**<span data-ttu-id="8e9c8-114">Pour mettre à jour les informations de redirection d’URL à l’aide d’une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8e9c8-114">To update URL Redirection information by using Group Policy</span></span>**

1.  <span data-ttu-id="8e9c8-115">Modifiez la valeur de la clé de Registre multichaîne nommée `RedirectUrls` .</span><span class="sxs-lookup"><span data-stu-id="8e9c8-115">Edit the registry key multi-string value that is named `RedirectUrls`.</span></span> <span data-ttu-id="8e9c8-116">Cette valeur se trouve généralement sur:</span><span class="sxs-lookup"><span data-stu-id="8e9c8-116">This value is typically located at:</span></span>

    <span data-ttu-id="8e9c8-117">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="8e9c8-117">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

    <span data-ttu-id="8e9c8-118">Si vous ajoutez des URL à la clé de Registre, entrez-les une par ligne, comme requis lors de la création du package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-118">If you are adding URLs to the registry key, enter them one per line, as was required when you built the MED-V workspace package.</span></span> <span data-ttu-id="8e9c8-119">Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="8e9c8-119">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

2.  <span data-ttu-id="8e9c8-120">Déployez la clé de Registre mise à jour à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-120">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="8e9c8-121">Pour plus d’informations sur l’utilisation d’une stratégie de groupe, voir [installation de logiciels de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="8e9c8-121">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

<span data-ttu-id="8e9c8-122">**Remarques**  Cette méthode de modification des informations de redirection d’URL est une meilleure pratique MED-V.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-122">**Note** This method of editing URL redirection information is a MED-V best practice.</span></span>

 

<a href="" id="bkmk-edittext"></a>**<span data-ttu-id="8e9c8-123">Pour recréer l’espace de travail MED-V en utilisant un fichier texte d’URL mis à jour</span><span class="sxs-lookup"><span data-stu-id="8e9c8-123">To rebuild the MED-V workspace by using an updated URL text file</span></span>**

-   <span data-ttu-id="8e9c8-124">Un autre moyen d’ajouter et de supprimer des URL de la liste de redirection consiste à mettre à jour le fichier texte de redirection d’URL et à l’utiliser pour créer un nouvel espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-124">Another method of adding and removing URLs from the redirection list is to update the URL redirection text file and then use it to build a new MED-V workspace.</span></span> <span data-ttu-id="8e9c8-125">Vous pouvez ensuite redéployer l’espace de travail MED-V comme auparavant, à l’aide de votre processus de déploiement standard, tel qu’un système ESD.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-125">You can then redeploy the MED-V workspace as before, by using your standard process of deployment, such as an ESD system.</span></span>

    <span data-ttu-id="8e9c8-126">**Important**  Nous déconseillons cette méthode de modification des informations de redirection d’URL.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-126">**Important** We do not recommend this method of editing URL redirection information.</span></span> <span data-ttu-id="8e9c8-127">De plus, à chaque fois que vous redéploiez l’espace de travail MED-V dans votre entreprise, la première fois que vous devez réexécuter le programme d’installation, toutes les données enregistrées dans l’ordinateur virtuel sont perdues.</span><span class="sxs-lookup"><span data-stu-id="8e9c8-127">In addition, any time that you redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="8e9c8-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e9c8-128">Related topics</span></span>


[<span data-ttu-id="8e9c8-129">Comment tester la redirection d'URL</span><span class="sxs-lookup"><span data-stu-id="8e9c8-129">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="8e9c8-130">Gestion d'applications déployées sur les espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="8e9c8-130">Managing Applications Deployed to MED-V Workspaces</span></span>](managing-applications-deployed-to-med-v-workspaces.md)

[<span data-ttu-id="8e9c8-131">Créer un package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="8e9c8-131">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

 

 





