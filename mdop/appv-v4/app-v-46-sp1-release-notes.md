---
title: Notes de publication d'App-V4.6SP1
description: Notes de publication d'App-V4.6SP1
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808066"
---
# <span data-ttu-id="ed44d-103">Notes de publication d'App-V4.6SP1</span><span class="sxs-lookup"><span data-stu-id="ed44d-103">App-V 4.6 SP1 Release Notes</span></span>


<span data-ttu-id="ed44d-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="ed44d-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="ed44d-105">**Important**  Lisez attentivement ces notes de publication avant d’installer le système de gestion Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="ed44d-105">**Important** Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="ed44d-106">Ces notes de publication contiennent des informations qui vous permettent d’installer correctement la virtualisation des applications (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="ed44d-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="ed44d-107">Ce document contient des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="ed44d-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="ed44d-108">S’il existe une différence entre ces notes de publication et d’autres documents App-V, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="ed44d-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span>

 

## <span data-ttu-id="ed44d-109">Se protéger contre les failles de sécurité et les virus</span><span class="sxs-lookup"><span data-stu-id="ed44d-109">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="ed44d-110">Pour vous aider à vous protéger contre les failles de sécurité et les virus, il est important d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé.</span><span class="sxs-lookup"><span data-stu-id="ed44d-110">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="ed44d-111">Pour plus d’informations, consultez le [site Web de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) sur la sécurité ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="ed44d-111">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="ed44d-112">Problèmes connus liés à la virtualisation d’application 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="ed44d-112">Known Issues with Application Virtualization4.6 SP1</span></span>


<span data-ttu-id="ed44d-113">Cette section fournit les informations les plus récentes sur les problèmes liés à Microsoft Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="ed44d-113">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="ed44d-114">Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire.</span><span class="sxs-lookup"><span data-stu-id="ed44d-114">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="ed44d-115">Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ed44d-115">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="ed44d-116">Le chemin d’accès à partir de SPRT est perdu s’il ne se termine pas par une barre oblique (/)</span><span class="sxs-lookup"><span data-stu-id="ed44d-116">Path from SPRT is lost if it does not end in forward slash ( / )</span></span>

<span data-ttu-id="ed44d-117">Si le chemin d’accès dans une expression HREF dans un modèle de projet ne se termine pas par une barre oblique ( **/** ), le chemin d’accès généré n’inclut pas le chemin.</span><span class="sxs-lookup"><span data-stu-id="ed44d-117">When the path in an HREF in a project template does not end with a forward slash (**/**), the generated HREF does not include the path.</span></span> <span data-ttu-id="ed44d-118">Cela se produit lorsque l’utilisateur manipule manuellement le fichier **. SPRT** .</span><span class="sxs-lookup"><span data-stu-id="ed44d-118">This occurs when the user manually manipulates the **.sprt** file.</span></span> <span data-ttu-id="ed44d-119">Si vous utilisez le Sequencer, il ajoute toujours la barre oblique ( **/** ) après la trajectoire.</span><span class="sxs-lookup"><span data-stu-id="ed44d-119">If you use the sequencer it always adds the forward slash (**/**) after the path.</span></span>

<span data-ttu-id="ed44d-120">Solution de contournement Assurez-vous que l’adresse HREF comporte une barre oblique de fin ( **/** ).</span><span class="sxs-lookup"><span data-stu-id="ed44d-120">WORKAROUND Make sure that the HREF has a trailing forward slash (**/**).</span></span>

### <span data-ttu-id="ed44d-121">Le nom du dossier utilisateur ne correspond pas au nom du package</span><span class="sxs-lookup"><span data-stu-id="ed44d-121">User folder name do not correspond to the package name</span></span>

<span data-ttu-id="ed44d-122">Les dossiers contenant des fichiers user et global. pkg n’incluent plus le nom du package.</span><span class="sxs-lookup"><span data-stu-id="ed44d-122">Folders that contain user and global .pkg files no longer include the package name.</span></span> <span data-ttu-id="ed44d-123">Auparavant, le client App-V a utilisé pour utiliser le nom court du dossier racine du package 8,3 dans le cadre du nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="ed44d-123">Previously, the App-V client used to use the package root folder 8.3 short name as part of the folder name.</span></span> <span data-ttu-id="ed44d-124">Cela vous permet de l’identifier facilement.</span><span class="sxs-lookup"><span data-stu-id="ed44d-124">This lets you easily identify it.</span></span> <span data-ttu-id="ed44d-125">Lorsque vous utilisez le Sequencer App-V 4,6 SP1, le dossier racine du package 8,3 noms courts est désormais une chaîne aléatoire.</span><span class="sxs-lookup"><span data-stu-id="ed44d-125">When you use the App-V 4.6 SP1 sequencer, the package root folder 8.3 short names are now random strings.</span></span> <span data-ttu-id="ed44d-126">Ainsi, il est difficile d’identifier les dossiers contenant les fichiers **. pkg** du package sur l’ordinateur exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="ed44d-126">This makes it difficult to identify the folders that contain the package’s **.pkg** files on the computer that is running the App-V client.</span></span>

<span data-ttu-id="ed44d-127">Solution de contournement utilisez l’une des méthodes suivantes pour identifier les dossiers de packages plus facilement:</span><span class="sxs-lookup"><span data-stu-id="ed44d-127">WORKAROUND Use one of the following methods to more easily identify these package folders:</span></span>

1.  <span data-ttu-id="ed44d-128">Lorsque vous créez le package en utilisant le Sequencer, spécifiez un nom de dossier qui suit la Convention d’affectation de noms 8,3 pour le dossier d’application principal.</span><span class="sxs-lookup"><span data-stu-id="ed44d-128">When you create the package by using the Sequencer, specify a folder name that follows the 8.3 naming convention for the primary application folder.</span></span> <span data-ttu-id="ed44d-129">Ce nom sera utilisé comme partie intégrante du nom du dossier utilisateur, comme dans le cas de l’App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="ed44d-129">This name will then be used as part of the user folder name as was the case in App-V 4.6.</span></span>

2.  <span data-ttu-id="ed44d-130">Le fichier. sprj contient désormais une balise qui affiche la chaîne utilisée comme début du nom du dossier utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed44d-130">The .sprj file now contains a tag that displays the string that is used as the beginning of the user folder name.</span></span> <span data-ttu-id="ed44d-131">Vous pouvez utiliser l’élément **ShortName** de l’élément **PACKAGEROOTFOLDER** pour déterminer le nom.</span><span class="sxs-lookup"><span data-stu-id="ed44d-131">You can use the **SHORTNAME** element of the **PACKAGEROOTFOLDER** element to determine the name.</span></span>

### <span data-ttu-id="ed44d-132">Exécution de App-V 4,6 SP1 sur des ordinateurs dotés de plus de 64 processeurs</span><span class="sxs-lookup"><span data-stu-id="ed44d-132">Running App-V 4.6 SP1 on computers that have more than 64 processors</span></span>

<span data-ttu-id="ed44d-133">Lorsque vous exécutez App-V 4,6 SP1 sur des ordinateurs dotés de plus de 64 processeurs, le client App-V échoue.</span><span class="sxs-lookup"><span data-stu-id="ed44d-133">When you run App-V 4.6 SP1 on computers that have more than 64 processors installed, the App-V client fails.</span></span>

<span data-ttu-id="ed44d-134">Solution de contournement aucune.</span><span class="sxs-lookup"><span data-stu-id="ed44d-134">WORKAROUND None.</span></span> <span data-ttu-id="ed44d-135">Cette configuration n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ed44d-135">This configuration is not supported.</span></span> <span data-ttu-id="ed44d-136">Vous devez exécuter des ordinateurs App-V 4,6 SP1on dont le nombre est inférieur à 64 processeurs.</span><span class="sxs-lookup"><span data-stu-id="ed44d-136">You must run App-V 4.6 SP1on computers that have fewer than 64 processors.</span></span>

### <span data-ttu-id="ed44d-137">La mise à jour de la virtualisation des applications 4,6 SP1 n’est pas proposée pour les paramètres régionaux qui utilisent Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="ed44d-137">Application Virtualization 4.6 SP1 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="ed44d-138">Lorsque vous utilisez Microsoft Update, la mise à jour pour App-V 4,6 SP1 n’est pas disponible pour les paramètres régionaux de langue suivants:</span><span class="sxs-lookup"><span data-stu-id="ed44d-138">When you use Microsoft Update, the update for App-V 4.6 SP1 is not available for the following language locales:</span></span>

-   <span data-ttu-id="ed44d-139">Kazakh</span><span class="sxs-lookup"><span data-stu-id="ed44d-139">Kazakh</span></span>

-   <span data-ttu-id="ed44d-140">Hindi</span><span class="sxs-lookup"><span data-stu-id="ed44d-140">Hindi</span></span>

-   <span data-ttu-id="ed44d-141">Serbe-cyrillique</span><span class="sxs-lookup"><span data-stu-id="ed44d-141">Serbian-Cyrillic</span></span>

<span data-ttu-id="ed44d-142">Solution de contournement si vous utilisez Microsoft Windows Server Update Services (WSUS) utilisez la version anglaise de la mise à jour ou téléchargez la mise à jour à partir du catalogue Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="ed44d-142">WORKAROUND If you are using Microsoft Windows Server Update Services (WSUS) use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

### <span data-ttu-id="ed44d-143">Après avoir développé le package parent, vous ne pouvez pas séquencer un plug-in avec des composants côte à côte.</span><span class="sxs-lookup"><span data-stu-id="ed44d-143">After expanding the parent package, you cannot sequence a plug-in with side by side components</span></span>

<span data-ttu-id="ed44d-144">Lorsque vous développez un package parent en utilisant les **Outils**  /  **développer le package sur le système local** dans la console de Sequencer App-V et que vous séquencez un plug-in avec des composants côte à côte, une erreur d’installation est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ed44d-144">When you expand a parent package by using **Tools** / **Expand Package to Local System** in the App-V Sequencer console and you sequence a plug-in with side by side components, an installation error is returned.</span></span> <span data-ttu-id="ed44d-145">Exemple:</span><span class="sxs-lookup"><span data-stu-id="ed44d-145">For example:</span></span>

-   **<span data-ttu-id="ed44d-146">HRESULT 0x80073712</span><span class="sxs-lookup"><span data-stu-id="ed44d-146">HRESULT 0x80073712</span></span>**

<span data-ttu-id="ed44d-147">Cela est dû au moment où le Sequencer écrit le composant côte à côte dans le registre, mais n’efface pas la valeur de la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="ed44d-147">This is caused when the sequencer writes the side-by-side component to the registry but does not clear the value for the following registry key:</span></span>

<span data-ttu-id="ed44d-148">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="ed44d-148">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="ed44d-149">Solution de contournement après avoir développé le package parent sur l’ordinateur qui exécute le Sequencer, vous devez supprimer la valeur pour la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="ed44d-149">WORKAROUND After expanding the parent package on the computer that is running the sequencer, you have to delete the value for the following registry key:</span></span>

<span data-ttu-id="ed44d-150">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="ed44d-150">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="ed44d-151">Après avoir supprimé la valeur, séquencez le plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed44d-151">After you have deleted the value, sequence the plug-in.</span></span>

### <span data-ttu-id="ed44d-152">Informations de copyright des notes de publication</span><span class="sxs-lookup"><span data-stu-id="ed44d-152">Release Notes Copyright Information</span></span>

<span data-ttu-id="ed44d-153">Ce document est fourni «en l’absence».</span><span class="sxs-lookup"><span data-stu-id="ed44d-153">This document is provided “as-is”.</span></span> <span data-ttu-id="ed44d-154">Les informations et les modes d’affichage exprimés dans ce document, tels que les URL et les autres références de site Web Internet, risquent de changer sans préavis.</span><span class="sxs-lookup"><span data-stu-id="ed44d-154">Information and views expressed in this document, such as URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="ed44d-155">Vous assumez le risque d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ed44d-155">You bear the risk of using it.</span></span>

<span data-ttu-id="ed44d-156">Quelques exemples présentés dans les présentes sont fournis à titre indicatif uniquement et sont fictifs.</span><span class="sxs-lookup"><span data-stu-id="ed44d-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="ed44d-157">Aucune association ou connexion réelle ne doit être intentionnelle ou intentionnelle.</span><span class="sxs-lookup"><span data-stu-id="ed44d-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="ed44d-158">Ce document ne vous fournit aucun droit légal de propriété intellectuelle de tout produit Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ed44d-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="ed44d-159">Vous pouvez copier le présent document pour une utilisation interne à des fins de référence.</span><span class="sxs-lookup"><span data-stu-id="ed44d-159">You may copy and use this document for your internal, reference purposes.</span></span> <span data-ttu-id="ed44d-160">Vous pouvez modifier ce document à des fins de référence interne.</span><span class="sxs-lookup"><span data-stu-id="ed44d-160">You may modify this document for your internal, reference purposes.</span></span>



<span data-ttu-id="ed44d-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server et Windows Vista sont des marques commerciales du groupe Microsoft de sociétés.</span><span class="sxs-lookup"><span data-stu-id="ed44d-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="ed44d-162">Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="ed44d-162">All other trademarks are property of their respective owners.</span></span>

 

 





