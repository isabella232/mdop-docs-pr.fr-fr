---
title: Page d’options avancées de l’Assistant séquençage de la virtualisation de l’application
description: Page d’options avancées de l’Assistant séquençage de la virtualisation de l’application
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807970"
---
# <span data-ttu-id="59305-103">Page d’options avancées de l’Assistant séquençage de la virtualisation de l’application</span><span class="sxs-lookup"><span data-stu-id="59305-103">Application Virtualization Sequencing Wizard Advanced Options Page</span></span>


<span data-ttu-id="59305-104">Utilisez la page **Options avancées** de l’Assistant séquençage de l’application virtualisation des applications (App-V) pour spécifier des options avancées pour l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="59305-104">Use the **Advanced Options** page of the Application Virtualization (App-V) Sequencing Wizard to specify advanced options for the application to be installed.</span></span> <span data-ttu-id="59305-105">La page contient les éléments décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="59305-105">The page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="59305-106">Nom</span><span class="sxs-lookup"><span data-stu-id="59305-106">Name</span></span></th>
<th align="left"><span data-ttu-id="59305-107">Description</span><span class="sxs-lookup"><span data-stu-id="59305-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="59305-108">Taille du bloc</span><span class="sxs-lookup"><span data-stu-id="59305-108">Block Size</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-109">Utilisez cette valeur pour spécifier la taille des blocs dans lesquels le fichier SFT sera subdivisé en continu sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="59305-109">Use to specify the size of blocks that the SFT file will be divided into when streamed across a network.</span></span> <span data-ttu-id="59305-110">Tous les blocs égaux à la taille spécifiée; Toutefois, le dernier bloc peut avoir une taille inférieure à celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="59305-110">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="59305-111">Sélectionnez l’une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="59305-111">Select one of the following values:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="59305-112">4 KO</span><span class="sxs-lookup"><span data-stu-id="59305-112">4 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="59305-113">16 KO</span><span class="sxs-lookup"><span data-stu-id="59305-113">16 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="59305-114">32 KO</span><span class="sxs-lookup"><span data-stu-id="59305-114">32 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="59305-115">64 KO</span><span class="sxs-lookup"><span data-stu-id="59305-115">64 KB</span></span></strong></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="59305-116">Remarque</span><span class="sxs-lookup"><span data-stu-id="59305-116">Note</span></span></strong><br/><p><span data-ttu-id="59305-117">Lorsque vous sélectionnez une taille de bloc, tenez compte de la taille du fichier SFT et de la bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="59305-117">When you select a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="59305-118">Le flux d’un fichier dont la taille de blocs est plus petite prend plus de temps sur le réseau, mais nécessite moins de bande passante.</span><span class="sxs-lookup"><span data-stu-id="59305-118">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="59305-119">Les fichiers de tailles de blocs plus grandes peuvent être plus rapides, mais ils utilisent plus de bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="59305-119">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="59305-120">Dans le cadre de l’expérimentation, vous pouvez découvrir la taille maximale de bloc pour les applications en continu sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="59305-120">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="59305-121">Activer Microsoft Update lors de l’analyse</span><span class="sxs-lookup"><span data-stu-id="59305-121">Enable Microsoft Update During Monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-122">Autorise l’installation des mises à jour de Microsoft au cours de l’Assistant de séquençage&#39;la phase d’analyse s.</span><span class="sxs-lookup"><span data-stu-id="59305-122">Enables installation of Microsoft Updates during the Sequencing Wizard&#39;s monitoring phase.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="59305-123">Dll de REBASE</span><span class="sxs-lookup"><span data-stu-id="59305-123">Rebase DLLs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-124">Permet le remappage des bibliothèques de liens dynamiques prises en charge sur un espace contigu dans la RAM, de l’économie de mémoire et des performances améliorées.</span><span class="sxs-lookup"><span data-stu-id="59305-124">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM, saving memory and improving performance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="59305-125">Back</span><span class="sxs-lookup"><span data-stu-id="59305-125">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-126">Accède à l’Assistant séquençage&#39;la page précédente.</span><span class="sxs-lookup"><span data-stu-id="59305-126">Accesses the Sequencing Wizard&#39;s previous page.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="59305-127">Next</span><span class="sxs-lookup"><span data-stu-id="59305-127">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-128">Accède à l’Assistant séquençage&#39;à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="59305-128">Accesses the Sequencing Wizard&#39;s next page.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="59305-129">Annuler</span><span class="sxs-lookup"><span data-stu-id="59305-129">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-130">Arrêt de l’opération de l’Assistant séquençage.</span><span class="sxs-lookup"><span data-stu-id="59305-130">Terminates operation of the Sequencing Wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="59305-131">\ [Valeur du jeton de modèle \]</span><span class="sxs-lookup"><span data-stu-id="59305-131">\[Template Token Value\]</span></span>

<span data-ttu-id="59305-132">Utilisez la page **Options avancées** de l’Assistant séquençage d’App-V pour spécifier des options avancées pour l’application que vous séquençage.</span><span class="sxs-lookup"><span data-stu-id="59305-132">Use the **Advanced Options** page of the App-V Sequencing Wizard to specify advanced options for the application you are sequencing.</span></span> <span data-ttu-id="59305-133">Cette page contient les éléments décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="59305-133">This page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="59305-134">Nom</span><span class="sxs-lookup"><span data-stu-id="59305-134">Name</span></span></th>
<th align="left"><span data-ttu-id="59305-135">Description</span><span class="sxs-lookup"><span data-stu-id="59305-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="59305-136">Autoriser l’exécution de Microsoft Update lors du suivi</span><span class="sxs-lookup"><span data-stu-id="59305-136">Allow Microsoft Update to run during monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-137">Spécifie si les mises à jour logicielles doivent être appliquées à l’application lors de la phase d’analyse du séquençage des applications.</span><span class="sxs-lookup"><span data-stu-id="59305-137">Specifies whether software updates will be applied to the application during the monitoring phase of application sequencing.</span></span> <span data-ttu-id="59305-138">Cette option est utile si des mises à jour sont nécessaires pour terminer l’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="59305-138">This option is helpful if updates are required to successfully complete the application installation.</span></span> <span data-ttu-id="59305-139">Cette option n’est pas sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="59305-139">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="59305-140">Dll de REBASE</span><span class="sxs-lookup"><span data-stu-id="59305-140">Rebase Dlls</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-141">Permet le remappage des bibliothèques de liens dynamiques prises en charge sur un espace contigu dans la RAM.</span><span class="sxs-lookup"><span data-stu-id="59305-141">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM.</span></span> <span data-ttu-id="59305-142">La sélection de cette option peut vous aider à gérer la mémoire et améliorer les performances de l’application.</span><span class="sxs-lookup"><span data-stu-id="59305-142">Selecting this option can help manage memory and improve application performance.</span></span> <span data-ttu-id="59305-143">Cette option n’est pas sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="59305-143">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="59305-144">Back</span><span class="sxs-lookup"><span data-stu-id="59305-144">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-145">Permet d’accéder à la page précédente de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="59305-145">Goes to the previous page of the wizard.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="59305-146">Next</span><span class="sxs-lookup"><span data-stu-id="59305-146">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-147">Accède à la page suivante de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="59305-147">Goes to the next page of the wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="59305-148">Annuler</span><span class="sxs-lookup"><span data-stu-id="59305-148">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59305-149">Supprime les paramètres et quitte l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="59305-149">Discards the settings and exits the wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="59305-150">\ [Valeur du jeton de modèle \]</span><span class="sxs-lookup"><span data-stu-id="59305-150">\[Template Token Value\]</span></span>

## <span data-ttu-id="59305-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59305-151">Related topics</span></span>


[<span data-ttu-id="59305-152">Assistant de séquencement</span><span class="sxs-lookup"><span data-stu-id="59305-152">Sequencing Wizard</span></span>](sequencing-wizard.md)









