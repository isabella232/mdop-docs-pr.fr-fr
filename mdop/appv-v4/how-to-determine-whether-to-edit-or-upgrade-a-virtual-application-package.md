---
title: Procédure pour déterminer si un package d'application virtuelle doit être modifié ou mis à jour
description: Procédure pour déterminer si un package d'application virtuelle doit être modifié ou mis à jour
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807133"
---
# <span data-ttu-id="e8a45-103">Procédure pour déterminer si un package d'application virtuelle doit être modifié ou mis à jour</span><span class="sxs-lookup"><span data-stu-id="e8a45-103">How to Determine Whether to Edit or Upgrade a Virtual Application Package</span></span>


<span data-ttu-id="e8a45-104">Utilisez le tableau suivant pour déterminer si un package d’application virtuel peut être ouvert pour modification, si vous avez besoin de créer une nouvelle version du package, ou si l’une des options est disponible à l’aide du Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="e8a45-104">Use the following table to help determine whether a virtual application package can be opened for edit, whether you need to create a new version of the package, or whether either option is available, using the App-V Sequencer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8a45-105">Action</span><span class="sxs-lookup"><span data-stu-id="e8a45-105">Action</span></span></th>
<th align="left"><span data-ttu-id="e8a45-106">Ouvrir pour modification</span><span class="sxs-lookup"><span data-stu-id="e8a45-106">Open for edit</span></span></th>
<th align="left"><span data-ttu-id="e8a45-107">Ouvrir pour la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="e8a45-107">Open for upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-108">Afficher les propriétés du package.</span><span class="sxs-lookup"><span data-stu-id="e8a45-108">View package properties.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-109">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-109">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-110">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-110">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-111">Afficher l’historique des modifications de package.</span><span class="sxs-lookup"><span data-stu-id="e8a45-111">View package change history.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-112">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-112">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-113">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-113">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-114">Afficher les fichiers de package associés.</span><span class="sxs-lookup"><span data-stu-id="e8a45-114">View associated package files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-115">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-115">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-116">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-116">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-117">Modifier les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="e8a45-117">Edit registry settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-118">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-118">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-119">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-119">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-120">Passez en revue les paramètres de package supplémentaires (sauf les propriétés du fichier système d’exploitation).</span><span class="sxs-lookup"><span data-stu-id="e8a45-120">Review additional package settings (except operating system file properties).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-121">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-121">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-122">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-123">Créer un programme d’installation Windows (MSI) associé.</span><span class="sxs-lookup"><span data-stu-id="e8a45-123">Create associated Windows Installer (MSI).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-124">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-124">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-125">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-125">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-126">Modifiez le fichier OSD.</span><span class="sxs-lookup"><span data-stu-id="e8a45-126">Modify OSD file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-127">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-127">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-128">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-129">Compresser et décompresser un package.</span><span class="sxs-lookup"><span data-stu-id="e8a45-129">Compress and uncompress package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-130">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-130">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-131">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-132">Ajouter des associations de types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8a45-132">Add file type associations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-133">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-133">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-134">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-134">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-135">Renommer des raccourcis.</span><span class="sxs-lookup"><span data-stu-id="e8a45-135">Rename shortcuts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-136">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-136">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-137">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-137">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-138">Définissez l’état de clé de Registre virtualisé (override/Merge).</span><span class="sxs-lookup"><span data-stu-id="e8a45-138">Set virtualized registry key state (override / merge).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-139">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-139">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-140">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-140">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-141">Définir l’état de dossier virtualisé.</span><span class="sxs-lookup"><span data-stu-id="e8a45-141">Set virtualized folder state.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-142">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-142">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-143">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-143">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-144">Modifier les mappages du système de fichiers virtuel.</span><span class="sxs-lookup"><span data-stu-id="e8a45-144">Edit virtual file system mappings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-145">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-146">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-147">Examinez toutes les propriétés de fichier du système d’exploitation associées pour un package.</span><span class="sxs-lookup"><span data-stu-id="e8a45-147">Review all associated operating system file properties for a package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-148">Non</span><span class="sxs-lookup"><span data-stu-id="e8a45-148">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-149">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-150">Ajoutez d’autres services.</span><span class="sxs-lookup"><span data-stu-id="e8a45-150">Add additional services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-151">Non</span><span class="sxs-lookup"><span data-stu-id="e8a45-151">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-152">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-153">Ajoutez des fichiers supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e8a45-153">Add additional files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-154">Non</span><span class="sxs-lookup"><span data-stu-id="e8a45-154">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-155">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-156">Recueillez et configurez les descripteurs de sécurité associés.</span><span class="sxs-lookup"><span data-stu-id="e8a45-156">Collect and configure associated security descriptors.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-157">Non</span><span class="sxs-lookup"><span data-stu-id="e8a45-157">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-158">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-159">Appliquer des mises à jour de sécurité ou effectuer une mise à niveau vers une nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="e8a45-159">Apply security updates or upgrade to a new version.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-160">Non</span><span class="sxs-lookup"><span data-stu-id="e8a45-160">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-161">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-161">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-162">Ajoutez une autre application.</span><span class="sxs-lookup"><span data-stu-id="e8a45-162">Add an additional application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-163">Non</span><span class="sxs-lookup"><span data-stu-id="e8a45-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-164">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-164">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8a45-165">Appliquez les mises à jour qui nécessitent l’ouverture de l’application.</span><span class="sxs-lookup"><span data-stu-id="e8a45-165">Apply updates that require the application to open.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-166">Non</span><span class="sxs-lookup"><span data-stu-id="e8a45-166">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-167">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8a45-168">Appliquez les mises à jour qui nécessitent le redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e8a45-168">Apply updates that require the computer to restart.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-169">Non</span><span class="sxs-lookup"><span data-stu-id="e8a45-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8a45-170">Oui</span><span class="sxs-lookup"><span data-stu-id="e8a45-170">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e8a45-171">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="e8a45-171">Related topics</span></span>


[<span data-ttu-id="e8a45-172">Procédure pour modifier une application virtuelle existante</span><span class="sxs-lookup"><span data-stu-id="e8a45-172">How to Edit an Existing Virtual Application</span></span>](how-to-edit-an-existing-virtual-application.md)

[<span data-ttu-id="e8a45-173">Procédure pour mettre à niveau une application virtuelle existante</span><span class="sxs-lookup"><span data-stu-id="e8a45-173">How to Upgrade an Existing Virtual Application</span></span>](how-to-upgrade-an-existing-virtual-application.md)

 

 





