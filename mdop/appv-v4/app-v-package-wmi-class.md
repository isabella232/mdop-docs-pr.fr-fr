---
title: Classe WMI de package App-V
description: Classe WMI de package App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808050"
---
# <span data-ttu-id="e6f8e-103">Classe WMI de package App-V</span><span class="sxs-lookup"><span data-stu-id="e6f8e-103">App-V Package WMI Class</span></span>


<span data-ttu-id="e6f8e-104">Dans le client Application Virtualization (App-V), la classe de **package** est une classe WMI (Windows Management Instrumentation) qui représente tous les packages virtuels sur le client.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-104">In the Application Virtualization (App-V) Client, the **Package** class is a Windows Management Instrumentation (WMI) class that represents all the virtual packages on the client.</span></span> <span data-ttu-id="e6f8e-105">Les packages virtuels peuvent contenir plusieurs applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-105">The virtual packages can contain many virtual applications.</span></span>

## <span data-ttu-id="e6f8e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6f8e-106">Syntax</span></span>


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## <span data-ttu-id="e6f8e-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6f8e-107">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="e6f8e-108">Nom</span><span class="sxs-lookup"><span data-stu-id="e6f8e-108">Name</span></span>**  
<span data-ttu-id="e6f8e-109">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-109">Data type: **String**</span></span>

<span data-ttu-id="e6f8e-110">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-110">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-111">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-111">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-112">Nom convivial du package virtuel.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-112">The user-friendly name of the virtual package.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="e6f8e-113">Version</span><span class="sxs-lookup"><span data-stu-id="e6f8e-113">Version</span></span>**  
<span data-ttu-id="e6f8e-114">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-114">Data type: **String**</span></span>

<span data-ttu-id="e6f8e-115">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-115">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-116">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-116">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-117">Version du package virtuel.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-117">The version of the virtual package.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="e6f8e-118">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="e6f8e-118">PackageGUID</span></span>**  
<span data-ttu-id="e6f8e-119">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-119">Data type: **String**</span></span>

<span data-ttu-id="e6f8e-120">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-120">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-121">Qualificateurs: clé</span><span class="sxs-lookup"><span data-stu-id="e6f8e-121">Qualifiers: Key</span></span>

<span data-ttu-id="e6f8e-122">Identificateur GUID de la configuration du package et des fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-122">The GUID identifier of the package configuration and source files.</span></span>

<a href="" id="sftpath"></a>**<span data-ttu-id="e6f8e-123">SftPath</span><span class="sxs-lookup"><span data-stu-id="e6f8e-123">SftPath</span></span>**  
<span data-ttu-id="e6f8e-124">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-124">Data type: **String**</span></span>

<span data-ttu-id="e6f8e-125">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-125">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-126">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-126">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-127">Le chemin d’accès du fichier SFT.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-127">The file path of the SFT file.</span></span>

<a href="" id="totalsize"></a>**<span data-ttu-id="e6f8e-128">TotalSize</span><span class="sxs-lookup"><span data-stu-id="e6f8e-128">TotalSize</span></span>**  
<span data-ttu-id="e6f8e-129">Type de données: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-129">Data type: **UInt64**</span></span>

<span data-ttu-id="e6f8e-130">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-130">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-131">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-131">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-132">Taille totale du package virtuel, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-132">The total size of the virtual package, in kilobytes.</span></span>

<a href="" id="cachedsize"></a>**<span data-ttu-id="e6f8e-133">CachedSize</span><span class="sxs-lookup"><span data-stu-id="e6f8e-133">CachedSize</span></span>**  
<span data-ttu-id="e6f8e-134">Type de données: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-134">Data type: **UInt64**</span></span>

<span data-ttu-id="e6f8e-135">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-135">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-136">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-136">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-137">Taille totale du cache pour le package virtuel, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-137">The total size of the cache for the virtual package, in kilobytes.</span></span>

<a href="" id="launchsize"></a>**<span data-ttu-id="e6f8e-138">LaunchSize</span><span class="sxs-lookup"><span data-stu-id="e6f8e-138">LaunchSize</span></span>**  
<span data-ttu-id="e6f8e-139">Type de données: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-139">Data type: **UInt64**</span></span>

<span data-ttu-id="e6f8e-140">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-140">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-141">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-141">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-142">Taille totale du bloc de fonctionnalités principal du package virtuel, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-142">The total size of the virtual package’s primary feature block, in kilobytes.</span></span>

<a href="" id="cachedlaunchsize"></a>**<span data-ttu-id="e6f8e-143">CachedLaunchSize</span><span class="sxs-lookup"><span data-stu-id="e6f8e-143">CachedLaunchSize</span></span>**  
<span data-ttu-id="e6f8e-144">Type de données: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-144">Data type: **UInt64**</span></span>

<span data-ttu-id="e6f8e-145">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-145">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-146">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-146">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-147">Taille totale du bloc de fonctionnalités principal du package virtuel qui a été mis en cache, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-147">Total size of the virtual package’s primary feature block that has been cached, in kilobytes.</span></span>

<a href="" id="inuse"></a>**<span data-ttu-id="e6f8e-148">InUse</span><span class="sxs-lookup"><span data-stu-id="e6f8e-148">InUse</span></span>**  
<span data-ttu-id="e6f8e-149">Type de données: **booléen**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-149">Data type: **Boolean**</span></span>

<span data-ttu-id="e6f8e-150">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-150">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-151">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-151">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-152">**true** si une application virtuelle du package virtuel est en cours d’exécution; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-152">**true** if any virtual application in the virtual package is running; otherwise **false**.</span></span>

<a href="" id="locked"></a>**<span data-ttu-id="e6f8e-153">Verrouillé</span><span class="sxs-lookup"><span data-stu-id="e6f8e-153">Locked</span></span>**  
<span data-ttu-id="e6f8e-154">Type de données: **booléen**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-154">Data type: **Boolean**</span></span>

<span data-ttu-id="e6f8e-155">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-155">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-156">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-156">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-157">**true** si le package virtuel est verrouillé; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-157">**true** if the virtual package is locked; otherwise **false**.</span></span>

<a href="" id="cachedpercentage"></a>**<span data-ttu-id="e6f8e-158">CachedPercentage</span><span class="sxs-lookup"><span data-stu-id="e6f8e-158">CachedPercentage</span></span>**  
<span data-ttu-id="e6f8e-159">Type de données: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-159">Data type: **UInt16**</span></span>

<span data-ttu-id="e6f8e-160">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-160">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-161">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-161">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-162">Pourcentage des fichiers cache.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-162">The percentage of the cache files.</span></span> <span data-ttu-id="e6f8e-163">En fonction de la formule suivante: CachedSize/TotalSize × 100.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-163">Based on the following formula: CachedSize / TotalSize × 100.</span></span>

<a href="" id="versionguid"></a>**<span data-ttu-id="e6f8e-164">VersionGUID</span><span class="sxs-lookup"><span data-stu-id="e6f8e-164">VersionGUID</span></span>**  
<span data-ttu-id="e6f8e-165">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e6f8e-165">Data type: **String**</span></span>

<span data-ttu-id="e6f8e-166">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6f8e-166">Access type: Read-only</span></span>

<span data-ttu-id="e6f8e-167">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="e6f8e-167">Qualifiers: None</span></span>

<span data-ttu-id="e6f8e-168">Identificateur GUID de la version du package.</span><span class="sxs-lookup"><span data-stu-id="e6f8e-168">The GUID identifier of the package version.</span></span>

 

 





