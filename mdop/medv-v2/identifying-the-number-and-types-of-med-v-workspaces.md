---
title: Identifier le nombre et les types d'espaces de travail MED-V
description: Identifier le nombre et les types d'espaces de travail MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812251"
---
# <span data-ttu-id="d60fb-103">Identifier le nombre et les types d'espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="d60fb-103">Identifying the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="d60fb-104">MED-V crée un environnement virtuel pour exécuter des applications qui nécessitent Windows XP ou qui nécessitent une version d’Internet Explorer différente de la version de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="d60fb-104">MED-V creates a virtual environment for running applications that require Windows XP or that require a version of Internet Explorer that differs from the version on the host computer.</span></span> <span data-ttu-id="d60fb-105">Cet environnement virtuel est connu sous le nom d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-105">This virtual environment is known as a MED-V workspace.</span></span>

<span data-ttu-id="d60fb-106">En fonction des exigences de compatibilité des applications auxquelles votre organisation a fait appel dans le cadre de la migration vers Windows 7, seuls certains utilisateurs ou services peuvent nécessiter des espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-106">Depending on the application compatibility requirements faced by your organization as you migrate to Windows 7, only certain users or departments might require MED-V workspaces.</span></span> <span data-ttu-id="d60fb-107">Lorsque vous planifiez votre déploiement, vous devez déterminer le nombre d’espaces de travail MED-V requis au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="d60fb-107">As you plan your deployment, you have to determine the number of MED-V workspaces required in your enterprise.</span></span> <span data-ttu-id="d60fb-108">Vous devez également définir les exigences de chaque espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-108">You also have to define the requirements of each MED-V workspace.</span></span>

## <span data-ttu-id="d60fb-109">Identifier le nombre et les types d’espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="d60fb-109">Identify the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="d60fb-110">Identifiez les ordinateurs et groupes de votre entreprise pour lesquels vous allez créer des espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-110">Identify the computers and groups in your enterprise for which you will be creating MED-V workspaces.</span></span> <span data-ttu-id="d60fb-111">En règle générale, il s’agit des utilisateurs qui ont besoin d’accéder à ces applications qui ne peuvent pas être migrées vers Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d60fb-111">Typically, these are the users who require access to those applications that cannot be migrated to Windows 7.</span></span> <span data-ttu-id="d60fb-112">Identifiez les applications qui ne peuvent pas être migrées, ainsi que les utilisateurs qui ont besoin d’un espace de travail MED-V pour exécuter ces applications.</span><span class="sxs-lookup"><span data-stu-id="d60fb-112">Identify those applications that cannot be migrated and the users who require a MED-V workspace to run these applications.</span></span>

<span data-ttu-id="d60fb-113">Vous pouvez également disposer d’adresses intranet qui n’ont pas encore été optimisées pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d60fb-113">You might also have intranet addresses that have not yet been optimized for Windows 7.</span></span> <span data-ttu-id="d60fb-114">L’espace de travail MED-V fournit un navigateur Internet Explorer par le biais duquel les utilisateurs finaux peuvent améliorer l’accès à ces adresses Web qui ne sont pas encore prêtes pour la migration vers Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d60fb-114">The MED-V workspace provides an Internet Explorer browser through which end users can better access those web addresses that are not yet ready for the migration to Windows 7.</span></span> <span data-ttu-id="d60fb-115">Au fur et à mesure que vous préparez et planifiez votre déploiement MED-V, vous devrez identifier et compiler une liste des adresses URL pour les rediriger vers Internet Explorer sur l’ordinateur hôte vers Internet Explorer dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-115">As you are preparing and planning your MED-V deployment, you will have to identify and compile a list of the URL addresses to redirect from Internet Explorer on the host computer to Internet Explorer in the MED-V workspace.</span></span>

<span data-ttu-id="d60fb-116">Enfin, vous devez évaluer l’espace disque requis.</span><span class="sxs-lookup"><span data-stu-id="d60fb-116">Finally, you have to evaluate your disk space requirements.</span></span> <span data-ttu-id="d60fb-117">La plupart des espaces de travail MED-V sont de 2 gigaoctets (Go) ou plus.</span><span class="sxs-lookup"><span data-stu-id="d60fb-117">Most MED-V workspaces are 2 gigabytes (GB) or larger.</span></span> <span data-ttu-id="d60fb-118">L’espace disque disponible sur un système peut être consommé rapidement, selon le nombre d’utilisateurs et la configuration de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-118">The available disk space on a system can be consumed quickly, depending on the number of users and the configuration of MED-V.</span></span> <span data-ttu-id="d60fb-119">Par ailleurs, le mode de distribution préféré de votre entreprise peut nécessiter un espace supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d60fb-119">Also, your company’s preferred method of distribution can require additional space.</span></span> <span data-ttu-id="d60fb-120">En règle générale, vous devez libérer un minimum de 10 Go d’espace disque pour un espace de travail MED-V, mais cela peut varier considérablement en fonction de la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="d60fb-120">Generally, you should free a minimum of 10 GB of disk space for a MED-V workspace, but this varies greatly, depending on the size of the image.</span></span>

### <span data-ttu-id="d60fb-121">Calculer l’espace disque requis pour les espaces de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="d60fb-121">Calculate the Disk Space Requirements for MED-V Workspaces</span></span>

<span data-ttu-id="d60fb-122">Un espace de travail MED-V nécessite une mémoire et un espace disque de l’ordinateur hôte sur lequel il est installé.</span><span class="sxs-lookup"><span data-stu-id="d60fb-122">A MED-V workspace requires memory and disk space from the host computer on which it is installed.</span></span> <span data-ttu-id="d60fb-123">Un minimum de 2 Go d’espace disque est requis sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d60fb-123">At a minimum, 2 GB of disk space are required on the host.</span></span> <span data-ttu-id="d60fb-124">L’espace disque est variable et dépend du nombre d’applications et des données de l’espace de travail MED-V d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d60fb-124">Disk space is variable and depends on the number of applications and the data in a user’s MED-V workspace.</span></span>

<span data-ttu-id="d60fb-125">Nous vous recommandons d’utiliser un minimum de 10 Go d’espace disque pour MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-125">We recommend a minimum of 10 GB of disk space for MED-V.</span></span> <span data-ttu-id="d60fb-126">Ce montant vous permet d’accéder à un espace de travail Windows XP de base et aux applications et à la redirection Web de base.</span><span class="sxs-lookup"><span data-stu-id="d60fb-126">This amount allows for a basic Windows XP workspace and some basic installed applications and web redirection.</span></span> <span data-ttu-id="d60fb-127">Il fournit également de l’espace disponible pour le lecteur d’échange hôte.</span><span class="sxs-lookup"><span data-stu-id="d60fb-127">It also provides available space for the host swap drive.</span></span> <span data-ttu-id="d60fb-128">Dans une configuration de base, MED-V et un espace de travail MED-V unique, qui consomment jusqu’à 8 Go.</span><span class="sxs-lookup"><span data-stu-id="d60fb-128">In a basic configuration, MED-V and a single deployed MED-V workspace consume as much as 6 to 8 GB.</span></span> <span data-ttu-id="d60fb-129">Si vous incluez un grand nombre d’applications sur l’espace de travail MED-V ou si vous avez plusieurs utilisateurs par ordinateur, vous pouvez utiliser le calcul suivant pour déterminer plus précisément l’espace disque requis par votre environnement MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-129">If you include lots of applications on the MED-V workspace or have more than one user per computer, then you can use the following calculation to more accurately determine the disk space your MED-V workspace requires:</span></span>

*<span data-ttu-id="d60fb-130">VHD de base + (utilisateur par ordinateur x (différence disque + état enregistré))</span><span class="sxs-lookup"><span data-stu-id="d60fb-130">Base VHD + (User per computer x (Difference Disk + Saved State))</span></span>*

<span data-ttu-id="d60fb-131">Pour calculer l’espace disque nécessaire, déterminez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="d60fb-131">To calculate the required disk space, determine the following:</span></span>

-   <span data-ttu-id="d60fb-132">**Taille du VHD de base** – disque dur virtuel utilisé pour créer l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-132">**Size of the base VHD** – the virtual hard disk that was used to create the MED-V workspace.</span></span>

    <span data-ttu-id="d60fb-133">**Important**  N’utilisez pas la taille de fichier. medv pour le calcul, car le fichier. medv est compressé.</span><span class="sxs-lookup"><span data-stu-id="d60fb-133">**Important** Do not use the .medv file size for your calculation because the .medv file is compressed.</span></span>

     

-   <span data-ttu-id="d60fb-134">**Utilisateurs par ordinateur** : MED-V crée un espace de travail MED-v pour chaque utilisateur sur un ordinateur; l’espace de travail MED-V utilise l’espace disque lorsque chaque utilisateur se connecte et que l’espace de travail MED-V est créé.</span><span class="sxs-lookup"><span data-stu-id="d60fb-134">**Users per computer** – MED-V creates a MED-V workspace for each user on a computer; the MED-V workspace consumes disk space as each user logs on and the MED-V workspace is created.</span></span>

-   <span data-ttu-id="d60fb-135">**Taille du disque de différenciation** , utilisée pour suivre la différence par rapport au disque dur virtuel de base.</span><span class="sxs-lookup"><span data-stu-id="d60fb-135">**Size of the differencing disk** – used to track the difference from the base VHD.</span></span> <span data-ttu-id="d60fb-136">Cette taille varie selon que vous ajoutez des applications et des mises à jour logicielles au disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d60fb-136">This size varies as you add applications and software updates to the virtual hard disk.</span></span> <span data-ttu-id="d60fb-137">Un disque de différenciation est créé pour chaque utilisateur MED-V lors du premier démarrage de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-137">A differencing disk is created for each MED-V user when they start MED-V for the first time.</span></span>

-   <span data-ttu-id="d60fb-138">**Taille du fichier d’état enregistré** , utilisé pour conserver l’État dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d60fb-138">**Size of the Saved State file** – used to maintain state in the virtual machine.</span></span> <span data-ttu-id="d60fb-139">En règle générale, il s’agit juste d’une taille supérieure à la RAM allouée pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d60fb-139">Typically, this is just a bit larger than the allocated RAM for the virtual machine.</span></span> <span data-ttu-id="d60fb-140">Par exemple, 1 Go de mémoire RAM allouée crée un fichier à propos de 1 081 000 Ko.</span><span class="sxs-lookup"><span data-stu-id="d60fb-140">For example, 1 GB of RAM allocated creates a file about 1,081,000 KB.</span></span>

<span data-ttu-id="d60fb-141">L’exemple suivant illustre un calcul basé sur trois utilisateurs d’un espace de travail MED-V qui dispose d’un disque dur virtuel de 2,6 Go:</span><span class="sxs-lookup"><span data-stu-id="d60fb-141">The following example shows a calculation based on three users of a MED-V workspace that has a 2.6 GB virtual hard disk:</span></span>

*<span data-ttu-id="d60fb-142">2,6 Go + (3 x (1.5 Go + 1)) = 10,1 Go</span><span class="sxs-lookup"><span data-stu-id="d60fb-142">2.6gb + (3 x (1.5gb + 1gb)) = 10.1gb</span></span>*

<span data-ttu-id="d60fb-143">**Remarques**  Une meilleure pratique pour MED-V consiste à calculer l’espace requis à l’aide d’un déploiement en laboratoire pour valider la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d60fb-143">**Note** A MED-V best practice is to calculate the required space by using a lab deployment to validate the requirements.</span></span>

 

### <span data-ttu-id="d60fb-144">Rechercher les fichiers pour déterminer la taille de fichier</span><span class="sxs-lookup"><span data-stu-id="d60fb-144">Locate the Files to Determine File Size</span></span>

<span data-ttu-id="d60fb-145">Les emplacements suivants contiennent les fichiers correspondant aux paramètres de l’ordinateur et de l’utilisateur:</span><span class="sxs-lookup"><span data-stu-id="d60fb-145">The following locations contain the files for the computer and user settings:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d60fb-146">Type</span><span class="sxs-lookup"><span data-stu-id="d60fb-146">Type</span></span></th>
<th align="left"><span data-ttu-id="d60fb-147">Location</span><span class="sxs-lookup"><span data-stu-id="d60fb-147">Location</span></span></th>
<th align="left"><span data-ttu-id="d60fb-148">Fichiers</span><span class="sxs-lookup"><span data-stu-id="d60fb-148">Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d60fb-149">VHD de base</span><span class="sxs-lookup"><span data-stu-id="d60fb-149">Base VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="d60fb-150">%ProgramData%\Microsoft\Medv\Workspace</span><span class="sxs-lookup"><span data-stu-id="d60fb-150">%ProgramData%\Microsoft\Medv\Workspace</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="d60fb-151">InternalName </em> . vhd-où <em> InternalName </em> est le nom du disque dur virtuel que vous avez sélectionné dans le module de création de package de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="d60fb-151">InternalName</em>.vhd - Where <em>InternalName</em> is the name of the virtual hard disk that you selected in the MED-V Workspace Packager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d60fb-152">Disque de différenciation</span><span class="sxs-lookup"><span data-stu-id="d60fb-152">Differencing Disk</span></span></p></td>
<td align="left"><p><span data-ttu-id="d60fb-153">Machines%LocalAppData%\Microsoft\MEDV\v2\Virtual</span><span class="sxs-lookup"><span data-stu-id="d60fb-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="d60fb-154">WorkspaceName </em> . vhd</span><span class="sxs-lookup"><span data-stu-id="d60fb-154">WorkspaceName</em>.vhd</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d60fb-155">Fichier d’état enregistré</span><span class="sxs-lookup"><span data-stu-id="d60fb-155">Saved State File</span></span></p></td>
<td align="left"><p><span data-ttu-id="d60fb-156">Machines%LocalAppData%\Microsoft\MEDV\v2\Virtual</span><span class="sxs-lookup"><span data-stu-id="d60fb-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="d60fb-157">WorkspaceName </em> . vsv</span><span class="sxs-lookup"><span data-stu-id="d60fb-157">WorkspaceName</em>.vsv</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d60fb-158">Calculer l’espace disque requis pour les espaces de travail MED-V partagés</span><span class="sxs-lookup"><span data-stu-id="d60fb-158">Calculate the Disk Space Requirements for Shared MED-V Workspaces</span></span>

<span data-ttu-id="d60fb-159">Si vous calculez un déploiement d’espace de travail MED-V partagé sur un ordinateur unique, le nombre d’utilisateurs par ordinateur dans votre calcul est toujours «1», car MED-V ne configure qu’un seul disque de différenciation pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d60fb-159">If you are calculating for a shared MED-V workspace deployment on a single computer, then the number of users per computer in your calculation is always “1” because MED-V only configures a single differencing disk for all users.</span></span>

<span data-ttu-id="d60fb-160">Vous pouvez trouver le disque de différenciation et le fichier d’état enregistré pour les espaces de travail MED-V partagés dans%ProgramData%\\Microsoft\\Medv\\AllUsers.</span><span class="sxs-lookup"><span data-stu-id="d60fb-160">You can find the differencing disk and the saved state file for shared MED-V workspaces in %ProgramData%\\Microsoft\\Medv\\AllUsers.</span></span>

## <span data-ttu-id="d60fb-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d60fb-161">Related topics</span></span>


[<span data-ttu-id="d60fb-162">Définir et planifier votre déploiement MED-V</span><span class="sxs-lookup"><span data-stu-id="d60fb-162">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

[<span data-ttu-id="d60fb-163">Planification de MED-V</span><span class="sxs-lookup"><span data-stu-id="d60fb-163">Planning for MED-V</span></span>](planning-for-med-v.md)

 

 





