---
title: Classe WMI de l'application App-V
description: Classe WMI de l'application App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809287"
---
# <span data-ttu-id="98958-103">Classe WMI de l'application App-V</span><span class="sxs-lookup"><span data-stu-id="98958-103">App-V Application WMI Class</span></span>


<span data-ttu-id="98958-104">Dans le client Application Virtualization (App-V), la classe **application** est une classe WMI (Windows Management Instrumentation) qui représente toutes les applications virtuelles sur le client.</span><span class="sxs-lookup"><span data-stu-id="98958-104">In the Application Virtualization (App-V) Client, the **Application** class is a Windows Management Instrumentation (WMI) class that represents all the virtual applications on the client.</span></span>

<span data-ttu-id="98958-105">La syntaxe suivante est simplifiée du code MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="98958-105">The following syntax is simplified from Managed Object Format (MOF) code.</span></span> <span data-ttu-id="98958-106">Le code inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="98958-106">The code includes all the inherited properties.</span></span>

## <span data-ttu-id="98958-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98958-107">Syntax</span></span>


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## <span data-ttu-id="98958-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98958-108">Requirements</span></span>


## <span data-ttu-id="98958-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="98958-109">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="98958-110">Nom</span><span class="sxs-lookup"><span data-stu-id="98958-110">Name</span></span>**  
<span data-ttu-id="98958-111">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98958-111">Data type: **String**</span></span>

<span data-ttu-id="98958-112">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="98958-112">Access type: Read-only</span></span>

<span data-ttu-id="98958-113">Qualificateurs: clé</span><span class="sxs-lookup"><span data-stu-id="98958-113">Qualifiers: Key</span></span>

<span data-ttu-id="98958-114">Nom d’affichage de l’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="98958-114">The display name of the virtual application.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="98958-115">Version</span><span class="sxs-lookup"><span data-stu-id="98958-115">Version</span></span>**  
<span data-ttu-id="98958-116">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98958-116">Data type: **String**</span></span>

<span data-ttu-id="98958-117">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="98958-117">Access type: Read-only</span></span>

<span data-ttu-id="98958-118">Qualificateurs: clé</span><span class="sxs-lookup"><span data-stu-id="98958-118">Qualifiers: Key</span></span>

<span data-ttu-id="98958-119">Version de l’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="98958-119">The version of the virtual application.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="98958-120">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="98958-120">PackageGUID</span></span>**  
<span data-ttu-id="98958-121">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98958-121">Data type: **String**</span></span>

<span data-ttu-id="98958-122">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="98958-122">Access type: Read-only</span></span>

<span data-ttu-id="98958-123">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="98958-123">Qualifiers: None</span></span>

<span data-ttu-id="98958-124">GUID du package auquel l’application virtuelle est associée.</span><span class="sxs-lookup"><span data-stu-id="98958-124">The GUID of the package that the virtual application is associated with.</span></span>

<a href="" id="lastlaunchonsystem"></a>**<span data-ttu-id="98958-125">LastLaunchOnSystem</span><span class="sxs-lookup"><span data-stu-id="98958-125">LastLaunchOnSystem</span></span>**  
<span data-ttu-id="98958-126">Type de données: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="98958-126">Data type: **DateTime**</span></span>

<span data-ttu-id="98958-127">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="98958-127">Access type: Read-only</span></span>

<span data-ttu-id="98958-128">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="98958-128">Qualifiers: None</span></span>

<span data-ttu-id="98958-129">La date et l’heure auxquelles l’application virtuelle a été lancée pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="98958-129">The last date and time that the virtual application was launched.</span></span>

<a href="" id="globalrunningcount"></a>**<span data-ttu-id="98958-130">GlobalRunningCount</span><span class="sxs-lookup"><span data-stu-id="98958-130">GlobalRunningCount</span></span>**  
<span data-ttu-id="98958-131">Type de données: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98958-131">Data type: **UInt32**</span></span>

<span data-ttu-id="98958-132">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="98958-132">Access type: Read-only</span></span>

<span data-ttu-id="98958-133">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="98958-133">Qualifiers: None</span></span>

<span data-ttu-id="98958-134">Nombre d’instances en cours d’exécution de l’application virtuelle démarrées directement.</span><span class="sxs-lookup"><span data-stu-id="98958-134">A count of the running instances of the virtual application that were started directly.</span></span>

<a href="" id="loading"></a>**<span data-ttu-id="98958-135">Chargement</span><span class="sxs-lookup"><span data-stu-id="98958-135">Loading</span></span>**  
<span data-ttu-id="98958-136">Type de données: **booléen**</span><span class="sxs-lookup"><span data-stu-id="98958-136">Data type: **Boolean**</span></span>

<span data-ttu-id="98958-137">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="98958-137">Access type: Read-only</span></span>

<span data-ttu-id="98958-138">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="98958-138">Qualifiers: None</span></span>

<span data-ttu-id="98958-139">**true** si l’application virtuelle est en cours de démarrage; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="98958-139">**true** if the virtual application is being started; otherwise **false**.</span></span>

<a href="" id="originalosdpath"></a>**<span data-ttu-id="98958-140">OriginalOsdPath</span><span class="sxs-lookup"><span data-stu-id="98958-140">OriginalOsdPath</span></span>**  
<span data-ttu-id="98958-141">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98958-141">Data type: **String**</span></span>

<span data-ttu-id="98958-142">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="98958-142">Access type: Read-only</span></span>

<span data-ttu-id="98958-143">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="98958-143">Qualifiers: None</span></span>

<span data-ttu-id="98958-144">Le chemin d’accès au fichier d’OSD enregistré dans le client App-V.</span><span class="sxs-lookup"><span data-stu-id="98958-144">The original file path of the OSD file that was registered with the App-V Client.</span></span>

<a href="" id="cachedosdpath"></a>**<span data-ttu-id="98958-145">CachedOsdPath</span><span class="sxs-lookup"><span data-stu-id="98958-145">CachedOsdPath</span></span>**  
<span data-ttu-id="98958-146">Type de données: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="98958-146">Data type: **String**</span></span>

<span data-ttu-id="98958-147">Type d’accès: lecture seule</span><span class="sxs-lookup"><span data-stu-id="98958-147">Access type: Read-only</span></span>

<span data-ttu-id="98958-148">Qualificateurs: aucun</span><span class="sxs-lookup"><span data-stu-id="98958-148">Qualifiers: None</span></span>

<span data-ttu-id="98958-149">Le chemin d’accès du fichier OSD si le client App-V a mis en cache le fichier OSD en local.</span><span class="sxs-lookup"><span data-stu-id="98958-149">The file path of the OSD file if the App-V Client has cached the OSD file locally.</span></span>

 

 





