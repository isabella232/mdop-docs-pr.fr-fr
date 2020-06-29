---
title: Synchroniser les événements du déclencheur pour UE-V2.x
description: Synchroniser les événements du déclencheur pour UE-V2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811970"
---
# <span data-ttu-id="1e981-103">Synchroniser les événements du déclencheur pour UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="1e981-103">Sync Trigger Events for UE-V 2.x</span></span>


<span data-ttu-id="1e981-104">Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 vous permet de synchroniser vos paramètres d’application et de Windows sur tous les appareils joints à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="1e981-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 lets you synchronize your application and Windows settings across all your domain-joined devices.</span></span> <span data-ttu-id="1e981-105">Les *événements de déclencheurs de synchronisation* déterminent à quel moment UE-V agent synchronise ces paramètres avec l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="1e981-105">*Sync trigger events* define when the UE-V Agent synchronizes those settings with the settings storage location.</span></span> <span data-ttu-id="1e981-106">UE-V 2 introduit une nouvelle *méthode de synchronisation* appelée *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="1e981-106">UE-V 2 introduces a new *Sync Method* called the *SyncProvider*.</span></span> <span data-ttu-id="1e981-107">Pour plus d’informations sur la configuration de la méthode de synchronisation, voir [méthodes de synchronisation pour UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="1e981-107">For more information about Sync Method configuration, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="1e981-108">Événements du déclencheur de synchronisation UE-V 2</span><span class="sxs-lookup"><span data-stu-id="1e981-108">UE-V 2 Sync Trigger Events</span></span>


<span data-ttu-id="1e981-109">Le tableau suivant décrit les événements de déclenchement des paramètres Windows et applications classiques.</span><span class="sxs-lookup"><span data-stu-id="1e981-109">The following table explains the trigger events for classic applications and Windows settings.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1e981-110">Événement déclencheur UE-V 2</span><span class="sxs-lookup"><span data-stu-id="1e981-110">UE-V 2 Trigger Event</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1e981-111">PowerSchool = SyncProvider</span><span class="sxs-lookup"><span data-stu-id="1e981-111">SyncMethod=SyncProvider</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="1e981-112">PowerSchool = aucun</span><span class="sxs-lookup"><span data-stu-id="1e981-112">SyncMethod=None</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1e981-113">Connexion Windows</span><span class="sxs-lookup"><span data-stu-id="1e981-113">Windows Logon</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1e981-114">Les paramètres d’application et de fenêtre sont importés dans le cache local à partir de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="1e981-114">Application and Windows settings are imported to the local cache from the settings storage location.</span></span></p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)"><span data-ttu-id="1e981-115">Les paramètres Windows asynchrones </a> sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="1e981-115">Asynchronous Windows settings</a> are applied.</span></span></p></li>
<li><p><span data-ttu-id="1e981-116">Les paramètres Windows synchrones seront appliqués lors de la prochaine connexion Windows.</span><span class="sxs-lookup"><span data-stu-id="1e981-116">Synchronous Windows settings will be applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="1e981-117">Les paramètres de l’application seront appliqués au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="1e981-117">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1e981-118">Les paramètres d’application et de fenêtre sont lus directement à partir de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="1e981-118">Application and Windows settings are read directly from the settings storage location.</span></span></p></li>
<li><p><span data-ttu-id="1e981-119">Les paramètres de fenêtre asynchrones et synchrones sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="1e981-119">Asynchronous and synchronous Windows settings are applied.</span></span></p></li>
<li><p><span data-ttu-id="1e981-120">Les paramètres de l’application seront appliqués au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="1e981-120">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1e981-121">Déconnexion Windows</span><span class="sxs-lookup"><span data-stu-id="1e981-121">Windows Logoff</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1e981-122">Stocker les modifications localement et mettre en cache et copier les paramètres de fenêtre asynchrones et synchrones sur le serveur emplacement de stockage des paramètres, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1e981-122">Store changes locally and cache and copy asynchronous and synchronous Windows settings to the settings storage location server, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e981-123">Stocker les modifications apportées à l’emplacement de stockage des paramètres Windows asynchrones et synchrones</span><span class="sxs-lookup"><span data-stu-id="1e981-123">Store changes to asynchronous and synchronous Windows settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1e981-124">Windows Connect (RDP)/déverrouiller</span><span class="sxs-lookup"><span data-stu-id="1e981-124">Windows Connect (RDP) / Unlock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1e981-125">Synchronisez les paramètres Windows asynchrones à partir de l’emplacement de stockage des paramètres au cache local, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1e981-125">Synchronize any asynchronous Windows settings from settings storage location to local cache, if available.</span></span></p>
<p><span data-ttu-id="1e981-126">Appliquer les paramètres Windows mis en cache</span><span class="sxs-lookup"><span data-stu-id="1e981-126">Apply cached Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e981-127">Télécharger et appliquer des paramètres Windows asynchrones à partir de l’emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="1e981-127">Download and apply asynchronous windows settings from settings storage location</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1e981-128">Déconnexion Windows (RDP)/verrouillage</span><span class="sxs-lookup"><span data-stu-id="1e981-128">Windows Disconnect (RDP) / Lock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1e981-129">Stocker les modifications apportées aux paramètres Windows asynchrones dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="1e981-129">Store asynchronous Windows settings changes to the local cache.</span></span></p>
<p><span data-ttu-id="1e981-130">Synchroniser les paramètres Windows asynchrones du cache local à l’emplacement de stockage des paramètres, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1e981-130">Synchronize any asynchronous Windows settings from the local cache to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e981-131">Stocker les modifications des paramètres Windows asynchrones dans l’emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="1e981-131">Store asynchronous Windows settings changes to the settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1e981-132">Démarrage de l’application</span><span class="sxs-lookup"><span data-stu-id="1e981-132">Application start</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1e981-133">Appliquer des paramètres d’application à partir du cache local au démarrage de l’application</span><span class="sxs-lookup"><span data-stu-id="1e981-133">Apply application settings from local cache as the application starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e981-134">Appliquer des paramètres d’application à partir de l’emplacement de stockage des paramètres au démarrage de l’application</span><span class="sxs-lookup"><span data-stu-id="1e981-134">Apply application settings from settings storage location as the application starts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1e981-135">Application se ferme</span><span class="sxs-lookup"><span data-stu-id="1e981-135">Application closes</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1e981-136">Enregistrez les modifications apportées aux paramètres d’application dans le cache local et copiez les paramètres dans l’emplacement de stockage des paramètres, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1e981-136">Store any application settings changes to the local cache and copy settings to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e981-137">Enregistrer les modifications apportées aux paramètres d’application dans l’emplacement de stockage des paramètres</span><span class="sxs-lookup"><span data-stu-id="1e981-137">Store any application settings changes to settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="1e981-138">La tâche planifiée du contrôleur de synchronisation ou «synchroniser maintenant» est exécutée à partir du centre de paramètres de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="1e981-138">Sync Controller Scheduled Task or “Sync Now” is run from the Company Settings Center</span></span></strong></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="1e981-139">Les paramètres d’application et de fenêtre sont synchronisés entre l’emplacement de stockage des paramètres et le cache local.</span><span class="sxs-lookup"><span data-stu-id="1e981-139">Application and Windows settings are synchronized between the settings storage location and the local cache.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1e981-140">Remarque</span><span class="sxs-lookup"><span data-stu-id="1e981-140">Note</span></span></strong><br/><p><span data-ttu-id="1e981-141">Les modifications apportées aux paramètres ne sont pas mises en cache localement avant la fermeture d’une application.</span><span class="sxs-lookup"><span data-stu-id="1e981-141">Settings changes are not cached locally until an application closes.</span></span> <span data-ttu-id="1e981-142">Ce déclencheur n’exporte pas les modifications apportées à une application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1e981-142">This trigger will not export changes made to a currently running application.</span></span></p>
<p><span data-ttu-id="1e981-143">Pour les paramètres Windows, cela signifie que les modifications apportées ne seront pas mises en cache localement et exportées jusqu’à ce que le verrouillage suivant (asynchrone ou synchrone et asynchrone) soit mis en cache.</span><span class="sxs-lookup"><span data-stu-id="1e981-143">For Windows settings, this means that any changes will not be cached locally and exported until the next Lock (Asynchronous) or Logoff (Asynchronous and Synchronous).</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="1e981-144">Les paramètres sont appliqués dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="1e981-144">Settings are applied in these cases:</span></span></p>
<ul>
<li><p><span data-ttu-id="1e981-145">Les paramètres Windows asynchrones sont directement appliqués.</span><span class="sxs-lookup"><span data-stu-id="1e981-145">Asynchronous Windows settings are applied directly.</span></span></p></li>
<li><p><span data-ttu-id="1e981-146">Les paramètres de l’application sont appliqués au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="1e981-146">Application settings are applied when the application starts.</span></span></p></li>
<li><p><span data-ttu-id="1e981-147">Les paramètres Windows asynchrones et synchrones sont appliqués lors du prochain ouverture de session Windows.</span><span class="sxs-lookup"><span data-stu-id="1e981-147">Both asynchronous and synchronous Windows settings are applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="1e981-148">Les paramètres de l’application Windows (AppX) s’appliquent lors de l’actualisation suivante.</span><span class="sxs-lookup"><span data-stu-id="1e981-148">Windows app (AppX) settings are applied during the next refresh.</span></span> <span data-ttu-id="1e981-149"><a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)"> </a> Pour plus d’informations, voir surveiller les paramètres d’application.</span><span class="sxs-lookup"><span data-stu-id="1e981-149">See <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Monitor Application Settings</a> for more information.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1e981-150">N/A</span><span class="sxs-lookup"><span data-stu-id="1e981-150">NA</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1e981-151">Paramètres asynchrones mis à jour dans le magasin distant \*</span><span class="sxs-lookup"><span data-stu-id="1e981-151">Asynchronous Settings updated on remote store\*</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1e981-152">Chargez et appliquez de nouveaux paramètres asynchrones à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="1e981-152">Load and apply new asynchronous settings from the cache.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1e981-153">Charger et appliquer des paramètres à partir du serveur central</span><span class="sxs-lookup"><span data-stu-id="1e981-153">Load and apply settings from central server</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="1e981-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e981-154">Related topics</span></span>


[<span data-ttu-id="1e981-155">Informations techniques de référence sur UE-V2.x</span><span class="sxs-lookup"><span data-stu-id="1e981-155">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

[<span data-ttu-id="1e981-156">Modification de la fréquence des tâches planifiées UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="1e981-156">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[<span data-ttu-id="1e981-157">Choisissez la méthode de configuration pour UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="1e981-157">Choose the Configuration Method for UE-V 2.x</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)









