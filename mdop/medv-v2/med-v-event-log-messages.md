---
title: Messages du journal des événements MED-V
description: Messages du journal des événements MED-V
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809738"
---
# <span data-ttu-id="7adca-103">Messages du journal des événements MED-V</span><span class="sxs-lookup"><span data-stu-id="7adca-103">MED-V Event Log Messages</span></span>


<span data-ttu-id="7adca-104">Les fichiers journaux pour Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 fournissent des informations détaillées sur le déploiement et la gestion de MED-V au sein de votre entreprise et permettent de vérifier les fonctionnalités ou d’aider à résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="7adca-104">The log files for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 provide detailed information about how to deploy and manage MED-V in your enterprise and help verify functionality or help troubleshoot issues.</span></span>

## <span data-ttu-id="7adca-105">ID d’événement</span><span class="sxs-lookup"><span data-stu-id="7adca-105">Event IDs</span></span>


<span data-ttu-id="7adca-106">Voici une liste des ID d’événement MED-V qui vous aideront à résoudre les problèmes que vous pouvez rencontrer lors du déploiement ou de la gestion de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-106">The following are a list of MED-V event IDs to help troubleshoot issues that you might encounter when you deploy or manage MED-V.</span></span>

### <span data-ttu-id="7adca-107">FTS</span><span class="sxs-lookup"><span data-stu-id="7adca-107">Fts</span></span>

<span data-ttu-id="7adca-108">Affiche les ID d’événement pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="7adca-108">Shows the event IDs for first time setup.</span></span>

### <span data-ttu-id="7adca-109">ID d’événement 3066</span><span class="sxs-lookup"><span data-stu-id="7adca-109">Event ID 3066</span></span>

<span data-ttu-id="7adca-110">Échec de l’opération de démarrage de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-110">Start virtual machine operation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-111">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-111">Description</span></span>**  
<span data-ttu-id="7adca-112">Il existe un problème potentiel avec le disque dur virtuel (VHD) que vous utilisez pour créer un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-112">A potential problem exists with the virtual hard disk (VHD) that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-113">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-113">Solution</span></span>**  
<span data-ttu-id="7adca-114">Vérifiez que vous pouvez créer une machine virtuelle avec le disque dur virtuel pour MED-V et qu’elle peut être démarrée.</span><span class="sxs-lookup"><span data-stu-id="7adca-114">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="7adca-115">ID d’événement 3071</span><span class="sxs-lookup"><span data-stu-id="7adca-115">Event ID 3071</span></span>

<span data-ttu-id="7adca-116">Échec de la préparation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-116">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-117">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-117">Description</span></span>**  
<span data-ttu-id="7adca-118">Un problème s’est produit lors de la première configuration qui aurait peut-être provoquée par différents problèmes.</span><span class="sxs-lookup"><span data-stu-id="7adca-118">A problem occurred with first time setup that might have been caused by many different issues.</span></span> <span data-ttu-id="7adca-119">Ces problèmes concernent la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="7adca-119">These include problems with network connectivity.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-120">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-120">Solution</span></span>**  
<span data-ttu-id="7adca-121">Redémarrez l’agent hôte MED-V pour réexécuter la première fois.</span><span class="sxs-lookup"><span data-stu-id="7adca-121">Restart the MED-V Host Agent to rerun first time setup.</span></span>

### <span data-ttu-id="7adca-122">ID d’événement 3078</span><span class="sxs-lookup"><span data-stu-id="7adca-122">Event ID 3078</span></span>

<span data-ttu-id="7adca-123">Échec de la préparation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-123">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-124">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-124">Description</span></span>**  
<span data-ttu-id="7adca-125">Il existe un problème potentiel avec le disque dur virtuel que vous utilisez pour créer un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-125">A potential problem exists with the VHD that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-126">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-126">Solution</span></span>**  
<span data-ttu-id="7adca-127">Vérifiez que vous pouvez créer une machine virtuelle avec le disque dur virtuel pour MED-V et qu’elle peut être démarrée.</span><span class="sxs-lookup"><span data-stu-id="7adca-127">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="7adca-128">ID d’événement 3079</span><span class="sxs-lookup"><span data-stu-id="7adca-128">Event ID 3079</span></span>

<span data-ttu-id="7adca-129">Nouvelle tentative de préparation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-129">Retrying virtual machine preparation.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-130">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-130">Description</span></span>**  
<span data-ttu-id="7adca-131">MED-V tente de préparer l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-131">MED-V is trying to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-132">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-132">Solution</span></span>**  
<span data-ttu-id="7adca-133">Aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="7adca-133">No action is required.</span></span> <span data-ttu-id="7adca-134">Fin de la configuration pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="7adca-134">Let first time setup finish.</span></span>

### <span data-ttu-id="7adca-135">ID d’événement 3080</span><span class="sxs-lookup"><span data-stu-id="7adca-135">Event ID 3080</span></span>

<span data-ttu-id="7adca-136">Le client a été arrêté lors de la préparation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-136">The client was stopped when preparing the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-137">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-137">Description</span></span>**  
<span data-ttu-id="7adca-138">MED-V s’arrête de manière inattendue lorsqu’il tente de préparer l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-138">MED-V stops unexpectedly when it tries to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-139">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-139">Solution</span></span>**  
<span data-ttu-id="7adca-140">Démarrer l’agent d’hébergement MED-V et permettre la fin de la configuration pour la première fois</span><span class="sxs-lookup"><span data-stu-id="7adca-140">Start the MED-V Host Agent and let first time setup complete</span></span>

### <span data-ttu-id="7adca-141">ID d’événement 3084</span><span class="sxs-lookup"><span data-stu-id="7adca-141">Event ID 3084</span></span>

<span data-ttu-id="7adca-142">Ordinateur virtuel non valide.</span><span class="sxs-lookup"><span data-stu-id="7adca-142">Virtual machine is not valid.</span></span> <span data-ttu-id="7adca-143">La première fois que vous devez réexécuter le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="7adca-143">First time setup needs to be re-run.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-144">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-144">Description</span></span>**  
<span data-ttu-id="7adca-145">L’agent d’hébergement MED-V a détecté un problème avec la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7adca-145">The MED-V Host Agent detected a problem with the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-146">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-146">Solution</span></span>**  
<span data-ttu-id="7adca-147">Aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="7adca-147">No action is required.</span></span> <span data-ttu-id="7adca-148">Fin de la configuration pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="7adca-148">Let first time setup finish.</span></span>

### <span data-ttu-id="7adca-149">ID d’événement 3099</span><span class="sxs-lookup"><span data-stu-id="7adca-149">Event ID 3099</span></span>

<span data-ttu-id="7adca-150">Échec de l’appel pour démarrer l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-150">Call to start virtual machine failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-151">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-151">Description</span></span>**  
<span data-ttu-id="7adca-152">Il existe un problème potentiel lié au VHD que vous utilisez pour créer un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-152">A potential problem exists with the VHD you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-153">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-153">Solution</span></span>**  
<span data-ttu-id="7adca-154">Vérifiez que vous pouvez créer une machine virtuelle avec le disque dur virtuel pour MED-V et qu’elle peut être ouverte.</span><span class="sxs-lookup"><span data-stu-id="7adca-154">Verify that you can create a virtual machine with the VHD for MED-V and that it can be opened.</span></span>

### <span data-ttu-id="7adca-155">Gestion de l’ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="7adca-155">VM Management</span></span>

### <span data-ttu-id="7adca-156">ID d’événement 4022</span><span class="sxs-lookup"><span data-stu-id="7adca-156">Event ID 4022</span></span>

<span data-ttu-id="7adca-157">VMManagerException erreur irrécupérable lors de la création de la commande sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7adca-157">VMManagerException Fatal error while issuing command to VM.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-158">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-158">Description</span></span>**  
<span data-ttu-id="7adca-159">L’utilisateur final a essayé de quitter MED-V en vous déconnectant ou en arrêtant l’hôte MED-V, et le paramètre de configuration VMTaskTimeout a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="7adca-159">The end user tried to exit MED-V by logging off or by shutting down the MED-V host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-160">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-160">Solution</span></span>**  
<span data-ttu-id="7adca-161">Redémarrez MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-161">Restart MED-V.</span></span>

### <span data-ttu-id="7adca-162">ID d’événement 4028</span><span class="sxs-lookup"><span data-stu-id="7adca-162">Event ID 4028</span></span>

<span data-ttu-id="7adca-163">Dépassement du délai de l’opération VM.</span><span class="sxs-lookup"><span data-stu-id="7adca-163">VM Operation timed out.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-164">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-164">Description</span></span>**  
<span data-ttu-id="7adca-165">L’utilisateur final a essayé de quitter MED-V en vous déconnectant ou en arrêtant l’hôte, et le paramètre de configuration VMTaskTimeout a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="7adca-165">The end user tried to exit MED-V by logging off or by shutting down the host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-166">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-166">Solution</span></span>**  
<span data-ttu-id="7adca-167">Redémarrez MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-167">Restart MED-V.</span></span>

### <span data-ttu-id="7adca-168">ID d’événement 4038</span><span class="sxs-lookup"><span data-stu-id="7adca-168">Event ID 4038</span></span>

<span data-ttu-id="7adca-169">Vmsal publié un message d’erreur pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7adca-169">Vmsal posted an error message to the user.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-170">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-170">Description</span></span>**  
<span data-ttu-id="7adca-171">Un message d’erreur s’affiche à l’utilisateur final indiquant que MED-V n’a pas pu démarrer l’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7adca-171">An error message is displayed to the end user stating that MED-V could not start the virtual application.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-172">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-172">Solution</span></span>**  
<span data-ttu-id="7adca-173">Si l’erreur est journalisée plusieurs fois dans une ligne, arrêtez MED-V, puis connectez-vous à l’ordinateur virtuel à l’aide de la console de l’ordinateur virtuel Windows et essayez de démarrer l’application en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="7adca-173">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console and attempt to start the application in Full Screen.</span></span>

### <span data-ttu-id="7adca-174">ID d’événement 4040</span><span class="sxs-lookup"><span data-stu-id="7adca-174">Event ID 4040</span></span>

<span data-ttu-id="7adca-175">Les ajouts de recyclage car TerminalServices n’est pas initialisé dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="7adca-175">Recycling Additions because TerminalServices is not initialized in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-176">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-176">Description</span></span>**  
<span data-ttu-id="7adca-177">MED-V a redémarré l’ordinateur virtuel, car le service bureau à distance n’a pas été initialisé sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-177">MED-V rebooted the virtual machine because Remote Desktop Services was not initialized on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-178">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-178">Solution</span></span>**  
<span data-ttu-id="7adca-179">Si l’erreur est journalisée plusieurs fois dans une ligne, arrêtez MED-V et connectez-vous à l’ordinateur virtuel à l’aide de la console Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7adca-179">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="7adca-180">ID d’événement 4042</span><span class="sxs-lookup"><span data-stu-id="7adca-180">Event ID 4042</span></span>

<span data-ttu-id="7adca-181">Échec du recyclage des ajouts dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="7adca-181">Failed to recycle additions in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-182">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-182">Description</span></span>**  
<span data-ttu-id="7adca-183">MED-V n’a pas réussi à recycler les ajouts de machines virtuelles sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-183">MED-V failed to recycle virtual machine additions on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-184">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-184">Solution</span></span>**  
<span data-ttu-id="7adca-185">Si l’erreur est journalisée plusieurs fois dans une ligne, arrêtez MED-V et connectez-vous à l’ordinateur virtuel à l’aide de la console Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7adca-185">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="7adca-186">ID d’événement 4043</span><span class="sxs-lookup"><span data-stu-id="7adca-186">Event ID 4043</span></span>

<span data-ttu-id="7adca-187">Échec de la réinitialisation du mot de passe expiré dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-187">Failed to reset expired password in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-188">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-188">Description</span></span>**  
<span data-ttu-id="7adca-189">L’utilisateur final n’a pas réinitialisé le mot de passe dans l’ordinateur virtuel avant son expiration.</span><span class="sxs-lookup"><span data-stu-id="7adca-189">The end user did not reset the password in the virtual machine before it expired.</span></span> <span data-ttu-id="7adca-190">Par conséquent, l’utilisateur n’est peut-être pas en mesure d’accéder aux ressources réseau ou d’enregistrer le fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="7adca-190">As a result, the user might not be able to access network resources or save work.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-191">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-191">Solution</span></span>**  
<span data-ttu-id="7adca-192">Arrêtez l’invité MED-V, puis redémarrez-le.</span><span class="sxs-lookup"><span data-stu-id="7adca-192">Shut down the MED-V guest and restart it.</span></span>

### <span data-ttu-id="7adca-193">Redirection d’URL</span><span class="sxs-lookup"><span data-stu-id="7adca-193">URL Redirection</span></span>

### <span data-ttu-id="7adca-194">ID d’événement 5005</span><span class="sxs-lookup"><span data-stu-id="7adca-194">Event ID 5005</span></span>

<span data-ttu-id="7adca-195">Impossible d’obtenir le nom de l’ordinateur virtuel de la configuration; ne peut pas lancer le navigateur invité.</span><span class="sxs-lookup"><span data-stu-id="7adca-195">Couldn’t get VM name from configuration; can’t launch guest browser.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-196">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-196">Description</span></span>**  
<span data-ttu-id="7adca-197">La redirection d’URL n’a pas pu obtenir le nom de l’espace de travail MED-V depuis la configuration.</span><span class="sxs-lookup"><span data-stu-id="7adca-197">URL Redirection could not obtain the MED-V workspace name from the configuration.</span></span> <span data-ttu-id="7adca-198">Par conséquent, il ne peut pas informer Windows Virtual PC de l’ouverture de l’URL redirigée dans le navigateur d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-198">As a result, it cannot inform Windows Virtual PC to open the redirected URL in the MED-V workspace browser.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-199">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-199">Solution</span></span>**  
<span data-ttu-id="7adca-200">Assurez-vous que le nom de l’espace de travail MED-V est défini et qu’il correspond à un nom de machine virtuelle dans l’annuaire de l' &lt; *utilisateur*C:\\Users\\ &gt; \\Virtual.</span><span class="sxs-lookup"><span data-stu-id="7adca-200">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="7adca-201">Le nom de l’espace de travail MED-V se trouve sur HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="7adca-201">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="7adca-202">Par exemple, si l’utilisateur est «mat» et que le nom de l’espace de travail est «mattsworkspace», la valeur de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name doit être «mattsworkspace» et il devrait y avoir un fichier nommé C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="7adca-202">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace", and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="7adca-203">ID d’événement 5006</span><span class="sxs-lookup"><span data-stu-id="7adca-203">Event ID 5006</span></span>

<span data-ttu-id="7adca-204">Échec de la création du serveur de canaux.</span><span class="sxs-lookup"><span data-stu-id="7adca-204">Failed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-205">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-205">Description</span></span>**  
<span data-ttu-id="7adca-206">Le service de redirection d’URL n’a pas pu créer le serveur de canaux pour communiquer avec Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7adca-206">The URL Redirection service could not create the pipe server to communicate with Internet Explorer.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-207">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-207">Solution</span></span>**  
<span data-ttu-id="7adca-208">Vérifiez les journaux d’événements système pour les tentatives de création d’un fichier ou d’une ressource dont le chemin d’accès commence comme suit: «\\\\.\\pipe\\MEDVUrlRedirectionPipe\_» et se termine par le nom d’utilisateur et le nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7adca-208">Check system event logs for attempts to create a file or resource whose path begins similar to the following: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" and ends with the user’s user name and domain name.</span></span> <span data-ttu-id="7adca-209">Si ce n’est pas le cas, redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7adca-209">If this is not present in the event log, restart the computer.</span></span>

### <span data-ttu-id="7adca-210">ConfigMgr (invité)</span><span class="sxs-lookup"><span data-stu-id="7adca-210">ConfigMgr (Guest)</span></span>

### <span data-ttu-id="7adca-211">ID d’événement 7001</span><span class="sxs-lookup"><span data-stu-id="7adca-211">Event ID 7001</span></span>

<span data-ttu-id="7adca-212">La mise en forme des données de configuration du réseau hôte n’est pas correcte.</span><span class="sxs-lookup"><span data-stu-id="7adca-212">The host network configuration data is not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-213">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-213">Description</span></span>**  
<span data-ttu-id="7adca-214">La configuration réseau reçue de l’hôte est une chaîne XML incorrectement mise en forme ou les informations réseau renvoyées par l’hôte ne peuvent pas être écrites dans un document XML.</span><span class="sxs-lookup"><span data-stu-id="7adca-214">Either the network configuration received from the host is an incorrectly formatted XML string, or the network information returned from the host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-215">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-215">Solution</span></span>**  
<span data-ttu-id="7adca-216">Redémarrez l’ordinateur hôte et l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-216">Restart the host computer and the virtual machine.</span></span>

### <span data-ttu-id="7adca-217">ID d’événement 7005</span><span class="sxs-lookup"><span data-stu-id="7adca-217">Event ID 7005</span></span>

<span data-ttu-id="7adca-218">Une modification apportée à la configuration du réseau hôte a été détectée, mais elle n’a pas pu être appliquée car les données de configuration du réseau hôte n’ont pas été correctement mises en forme.</span><span class="sxs-lookup"><span data-stu-id="7adca-218">A change to the host network configuration was detected, but was not able to be applied because the host network configuration data was not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-219">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-219">Description</span></span>**  
<span data-ttu-id="7adca-220">Une modification apportée à la configuration du réseau hôte a été communiquée à l’ordinateur virtuel, mais elle n’a pas pu être traitée dans l’ordinateur virtuel en raison d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="7adca-220">A change to the host network configuration was communicated to the virtual machine, but could not be processed in the virtual machine because of an error.</span></span> <span data-ttu-id="7adca-221">Cette erreur peut être provoquée par des données mises en forme de manière incorrecte ou par l’impossibilité de définir les informations dans l’instance CCMNetworkAdapter WMI (Windows Management Instrumentation).</span><span class="sxs-lookup"><span data-stu-id="7adca-221">This error could be caused by incorrectly formatted data or the inability to set the information into the Windows Management Instrumentation (WMI) CCMNetworkAdapter instance.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-222">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-222">Solution</span></span>**  
<span data-ttu-id="7adca-223">Redémarrez l’hôte et l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-223">Restart the host and virtual machine.</span></span>

### <span data-ttu-id="7adca-224">ConfigMgr (hôte)</span><span class="sxs-lookup"><span data-stu-id="7adca-224">ConfigMgr (Host)</span></span>

### <span data-ttu-id="7adca-225">ID d’événement 8006</span><span class="sxs-lookup"><span data-stu-id="7adca-225">Event ID 8006</span></span>

<span data-ttu-id="7adca-226">Ordinateur virtuel introuvable.</span><span class="sxs-lookup"><span data-stu-id="7adca-226">The virtual machine cannot be found.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-227">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-227">Description</span></span>**  
<span data-ttu-id="7adca-228">Windows Virtual PC 7 ne parvient pas à trouver l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-228">Windows Virtual PC 7 cannot locate the virtual machine.</span></span> <span data-ttu-id="7adca-229">Il est possible que l’ordinateur virtuel ait été supprimé, déplacé, supprimé ou que l’accès ait été refusé.</span><span class="sxs-lookup"><span data-stu-id="7adca-229">The virtual machine might have been deleted, moved, removed, or access was denied.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-230">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-230">Solution</span></span>**  
<span data-ttu-id="7adca-231">Réinstallez l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-231">Reinstall the virtual machine.</span></span>

### <span data-ttu-id="7adca-232">ID d’événement 8008</span><span class="sxs-lookup"><span data-stu-id="7adca-232">Event ID 8008</span></span>

<span data-ttu-id="7adca-233">Les informations de configuration réseau du poste de travail n’ont pas pu être récupérées.</span><span class="sxs-lookup"><span data-stu-id="7adca-233">The workstation's network configuration information could not be retrieved.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-234">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-234">Description</span></span>**  
<span data-ttu-id="7adca-235">Les informations de configuration du réseau n’ont pas pu être collectées à partir de l’hôte MED-V, probablement en raison d’une défaillance d’un appel système dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7adca-235">Network configuration information could not be collected from the MED-V host, most likely because of a system call failure in the .NET Framework.</span></span> <span data-ttu-id="7adca-236">Ce problème peut également se produire si les informations réseau renvoyées à partir de l’hôte MED-V ne peuvent pas être écrites dans un document XML.</span><span class="sxs-lookup"><span data-stu-id="7adca-236">This failure can also occur if the network information returned from the MED-V host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-237">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-237">Solution</span></span>**  
<span data-ttu-id="7adca-238">Redémarrez la station de travail hôte.</span><span class="sxs-lookup"><span data-stu-id="7adca-238">Restart the host workstation.</span></span>

### <span data-ttu-id="7adca-239">ID d’événement 8010</span><span class="sxs-lookup"><span data-stu-id="7adca-239">Event ID 8010</span></span>

<span data-ttu-id="7adca-240">Les données de configuration réseau n’ont pas pu être définies dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-240">The network configuration data could not be set in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-241">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-241">Description</span></span>**  
<span data-ttu-id="7adca-242">La traduction d’adresses réseau (NAT) MED-V hostnetwork n’a pas pu être communiquée à l’ordinateur virtuel, car c’est probablement parce que l’ordinateur virtuel est dans un état incorrect ou qu’il n’a pas été installé ou activé.</span><span class="sxs-lookup"><span data-stu-id="7adca-242">The MED-V hostnetwork address translation (NAT) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-243">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-243">Solution</span></span>**  
<span data-ttu-id="7adca-244">Fermez et redémarrez l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-244">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="7adca-245">Par ailleurs, il se peut que vous deviez réinstaller l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-245">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="7adca-246">ID d’événement 8011</span><span class="sxs-lookup"><span data-stu-id="7adca-246">Event ID 8011</span></span>

<span data-ttu-id="7adca-247">Échec de la réinitialisation des données de configuration du réseau dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-247">The network configuration data could not be reset in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-248">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-248">Description</span></span>**  
<span data-ttu-id="7adca-249">La configuration de hostnetwork MED-V (BRIDGEd) n’a pas pu être communiquée à l’ordinateur virtuel, probablement en raison du mauvais état de l’ordinateur virtuel ou des ajouts de PC Windows n’ont pas été installés ou activés.</span><span class="sxs-lookup"><span data-stu-id="7adca-249">The MED-V hostnetwork configuration (BRIDGED) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-250">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-250">Solution</span></span>**  
<span data-ttu-id="7adca-251">Fermez et redémarrez l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-251">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="7adca-252">Par ailleurs, il se peut que vous deviez réinstaller l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7adca-252">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="7adca-253">Redirection d’imprimante</span><span class="sxs-lookup"><span data-stu-id="7adca-253">Printer Redirection</span></span>

### <span data-ttu-id="7adca-254">ID d’événement 9001</span><span class="sxs-lookup"><span data-stu-id="7adca-254">Event ID 9001</span></span>

<span data-ttu-id="7adca-255">Erreur d’autorisation de fichier.</span><span class="sxs-lookup"><span data-stu-id="7adca-255">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-256">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-256">Description</span></span>**  
<span data-ttu-id="7adca-257">L’utilisateur final n’est pas autorisé à accéder au dossier requis pour ouvrir ou créer le fichier d’imprimante MED-V pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="7adca-257">The end user is not authorized to access the folder required to open or create the MED-V printer file for reading.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-258">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-258">Solution</span></span>**  
<span data-ttu-id="7adca-259">Vérifiez que le chemin d’accès User\\AppData\\ est accessible et que l’utilisateur est autorisé à lire et écrire dessus.</span><span class="sxs-lookup"><span data-stu-id="7adca-259">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="7adca-260">Par exemple, si l’utilisateur est «mat», le chemin d’accès C:\\Users\\Matt\\AppData\\ et tous les fichiers doivent avoir des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="7adca-260">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\, and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="7adca-261">Si tel est le cas, le chemin C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ et tous les fichiers qu’ils contiennent doivent avoir des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="7adca-261">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="7adca-262">ID d’événement 9002</span><span class="sxs-lookup"><span data-stu-id="7adca-262">Event ID 9002</span></span>

<span data-ttu-id="7adca-263">Erreur d’autorisation de fichier.</span><span class="sxs-lookup"><span data-stu-id="7adca-263">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-264">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-264">Description</span></span>**  
<span data-ttu-id="7adca-265">L’utilisateur final n’est pas autorisé à accéder au dossier requis pour ouvrir ou créer le fichier d’imprimante MED-V à des fins de rédaction.</span><span class="sxs-lookup"><span data-stu-id="7adca-265">The end user is not authorized to access the folder required to open or create the MED-V printer file for writing.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-266">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-266">Solution</span></span>**  
<span data-ttu-id="7adca-267">Assurez-vous que le chemin d’accès User\\AppData\\ est accessible et que l’utilisateur est autorisé à lire et écrire dessus.</span><span class="sxs-lookup"><span data-stu-id="7adca-267">Ensure that the User\\AppData\\ path can be accessed, and that the user has permission to read and write to it.</span></span> <span data-ttu-id="7adca-268">Par exemple, si l’utilisateur est «mat», le chemin d’accès C:\\Users\\Matt\\AppData\\ et tous les fichiers qu’il contient doivent avoir des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="7adca-268">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="7adca-269">Si tel est le cas, le chemin C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ et tous les fichiers qu’ils contiennent doivent avoir des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="7adca-269">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="7adca-270">ID d’événement 9004</span><span class="sxs-lookup"><span data-stu-id="7adca-270">Event ID 9004</span></span>

<span data-ttu-id="7adca-271">Impossible de créer le chemin d’accès pour le stockage des fichiers d’imprimante MEDV.</span><span class="sxs-lookup"><span data-stu-id="7adca-271">Could not create path for storing MEDV printer files.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-272">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-272">Description</span></span>**  
<span data-ttu-id="7adca-273">Le service de redirection d’imprimante n’a pas pu accéder aux fichiers ou créer des répertoires requis pour le stockage des informations d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="7adca-273">The printer redirection service could not access files or create directories required for storing the printer information.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-274">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-274">Solution</span></span>**  
<span data-ttu-id="7adca-275">Vérifiez que le chemin d’accès User\\AppData\\ est accessible et que l’utilisateur est autorisé à lire et écrire dessus.</span><span class="sxs-lookup"><span data-stu-id="7adca-275">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="7adca-276">Par exemple, si l’utilisateur est «mat», le chemin d’accès C:\\Users\\Matt\\AppData\\ et tous les fichiers qu’il contient doivent avoir des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="7adca-276">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="7adca-277">Si tel est le cas, le chemin C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ et tous les fichiers qu’ils contiennent doivent avoir des autorisations de lecture et d’écriture.</span><span class="sxs-lookup"><span data-stu-id="7adca-277">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="7adca-278">ID d’événement 9005</span><span class="sxs-lookup"><span data-stu-id="7adca-278">Event ID 9005</span></span>

<span data-ttu-id="7adca-279">Impossible d’obtenir le nom de l’ordinateur virtuel de la configuration; ne peut pas lancer le programme d’installation invité.</span><span class="sxs-lookup"><span data-stu-id="7adca-279">Couldn’t get VM name from configuration; cannot launch guest installer.</span></span> <span data-ttu-id="7adca-280">Impossible de mettre à jour MED-V: aucun réseau hôte détecté.</span><span class="sxs-lookup"><span data-stu-id="7adca-280">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-281">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-281">Description</span></span>**  
<span data-ttu-id="7adca-282">Le service de redirection d’imprimante n’a pas pu obtenir le nom de l’espace de travail MED-V à partir de la configuration MED-v et ne peut pas informer Windows Virtual PC du démarrage du programme d’installation sur l’invité MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-282">The printer redirection service was not able to obtain the MED-V workspace name from the MED-V configuration and cannot inform Windows Virtual PC to start the installer on the MED-V guest.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-283">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-283">Solution</span></span>**  
<span data-ttu-id="7adca-284">Assurez-vous que le nom de l’espace de travail MED-V est défini et qu’il correspond à un nom de machine virtuelle dans l’annuaire de l' &lt; *utilisateur*C:\\Users\\ &gt; \\Virtual.</span><span class="sxs-lookup"><span data-stu-id="7adca-284">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="7adca-285">Le nom de l’espace de travail MED-V se trouve sur HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span><span class="sxs-lookup"><span data-stu-id="7adca-285">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="7adca-286">Par exemple, si l’utilisateur est «mat» et que le nom de l’espace de travail est «mattsworkspace», la valeur de HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name doit être «mattsworkspace» et il devrait y avoir un fichier nommé C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span><span class="sxs-lookup"><span data-stu-id="7adca-286">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace" and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="7adca-287">Publication d’applications</span><span class="sxs-lookup"><span data-stu-id="7adca-287">Application Publishing</span></span>

### <span data-ttu-id="7adca-288">ID d’événement 10015</span><span class="sxs-lookup"><span data-stu-id="7adca-288">Event ID 10015</span></span>

<span data-ttu-id="7adca-289">Une erreur de système de fichiers s’est produite lors du processus de conciliation.</span><span class="sxs-lookup"><span data-stu-id="7adca-289">A file system error occurred during the reconcile process.</span></span> <span data-ttu-id="7adca-290">Le processus de rapprochement ne traitera pas le nom de fichier, &lt; *filename* &gt; mais continuera à traiter tout autre changement.</span><span class="sxs-lookup"><span data-stu-id="7adca-290">The reconcile process will not process the file &lt;*filename*&gt; but will continue to process any other changes.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-291">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-291">Description</span></span>**  
<span data-ttu-id="7adca-292">Un accès non autorisé ou une erreur d’e/s s’est produit lors de la création ou de la suppression d’un raccourci.</span><span class="sxs-lookup"><span data-stu-id="7adca-292">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-293">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-293">Solution</span></span>**  
<span data-ttu-id="7adca-294">Vérifiez que le chemin d’accès du fichier est accessible et que l’utilisateur dispose des autorisations nécessaires pour créer ou supprimer le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="7adca-294">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="7adca-295">ID d’événement 10021</span><span class="sxs-lookup"><span data-stu-id="7adca-295">Event ID 10021</span></span>

<span data-ttu-id="7adca-296">&lt; *Erreur d’erreur \ _information* &gt; pour l’opération d’opération de fichier &lt; *\ _name* &gt; sur le &lt; *nom du*fichier &gt; .</span><span class="sxs-lookup"><span data-stu-id="7adca-296">Error &lt;*error\_information*&gt; for file operation &lt;*operation\_name*&gt; on file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-297">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-297">Description</span></span>**  
<span data-ttu-id="7adca-298">Un accès non autorisé ou une erreur d’e/s s’est produit lors de la création ou de la suppression d’un raccourci.</span><span class="sxs-lookup"><span data-stu-id="7adca-298">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-299">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-299">Solution</span></span>**  
<span data-ttu-id="7adca-300">Vérifiez que le chemin d’accès du fichier est accessible et que l’utilisateur dispose des autorisations nécessaires pour créer ou supprimer le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="7adca-300">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="7adca-301">Correction invité</span><span class="sxs-lookup"><span data-stu-id="7adca-301">Guest Patching</span></span>

### <span data-ttu-id="7adca-302">ID d’événement 11001</span><span class="sxs-lookup"><span data-stu-id="7adca-302">Event ID 11001</span></span>

<span data-ttu-id="7adca-303">Message d’utilisation des tâches de réveil d’invité.</span><span class="sxs-lookup"><span data-stu-id="7adca-303">Guest wakeup task usage message.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-304">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-304">Description</span></span>**  
<span data-ttu-id="7adca-305">MedvHost.exe l’option/GuestWakeup est exécutée de manière incorrecte ou la commande est mise en forme de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="7adca-305">MedvHost.exe with the /GuestWakeup option was executed incorrectly, or the command is formatted incorrectly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-306">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-306">Solution</span></span>**  
<span data-ttu-id="7adca-307">Vérifiez que la commande est exécutée avec le format suivant:</span><span class="sxs-lookup"><span data-stu-id="7adca-307">Ensure that the command is executed with the following format:</span></span>

<span data-ttu-id="7adca-308">Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *espace de travail \ _name* &gt; " Where</span><span class="sxs-lookup"><span data-stu-id="7adca-308">Medvhost.exe /GuestWakeup /d:&lt; *duration\_in\_minutes*&gt; /v:”&lt; *workspace\_name*&gt;” where</span></span>

<span data-ttu-id="7adca-309">&lt;*durée \ _in \ _minutes* &gt; est le nombre de minutes pendant lesquelles l’ordinateur virtuel doit rester éveillé (la valeur par défaut est 240) et</span><span class="sxs-lookup"><span data-stu-id="7adca-309">&lt;*duration\_in\_minutes*&gt; is the number of minutes that the virtual machine should stay awake (default is 240) and</span></span>

<span data-ttu-id="7adca-310">&lt;*espace de travail \ _name* &gt; est le nom de l’ordinateur virtuel qui doit être réveillé.</span><span class="sxs-lookup"><span data-stu-id="7adca-310">&lt;*workspace\_name*&gt; is the name of the virtual machine that should be awakened.</span></span>

### <span data-ttu-id="7adca-311">ID d’événement 11002</span><span class="sxs-lookup"><span data-stu-id="7adca-311">Event ID 11002</span></span>

<span data-ttu-id="7adca-312">Impossible de mettre à jour MED-V: aucun réseau hôte détecté.</span><span class="sxs-lookup"><span data-stu-id="7adca-312">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-313">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-313">Description</span></span>**  
<span data-ttu-id="7adca-314">Le correctif invité n’a pas pu s’achever car aucune connexion réseau hôte n’a été détectée.</span><span class="sxs-lookup"><span data-stu-id="7adca-314">Guest patching could not finish because no host network connection was detected.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-315">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-315">Solution</span></span>**  
<span data-ttu-id="7adca-316">Connectez l’hôte MED-V à une connexion réseau active avant d’exécuter le correctif invité.</span><span class="sxs-lookup"><span data-stu-id="7adca-316">Connect the MED-V host to an active network connection before you run guest patching.</span></span>

### <span data-ttu-id="7adca-317">ID d’événement 11003</span><span class="sxs-lookup"><span data-stu-id="7adca-317">Event ID 11003</span></span>

<span data-ttu-id="7adca-318">Ne peut pas mettre à jour MED-V-hôte qui ne s’exécute pas sur un/C powerFailed pour créer un serveur de canaux.</span><span class="sxs-lookup"><span data-stu-id="7adca-318">Cannot update MED-V – Host not running on A/C powerFailed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-319">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-319">Description</span></span>**  
<span data-ttu-id="7adca-320">Le correctif invité n’a pas pu s’achever, car l’hôte semble fonctionner sur batterie plutôt que sur un cordon d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="7adca-320">Guest patching could not finish because the host appears to be running on battery power instead of from a power cord.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-321">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-321">Solution</span></span>**  
<span data-ttu-id="7adca-322">Connectez l’ordinateur hôte à un cordon d’alimentation avant d’exécuter le correctif invité.</span><span class="sxs-lookup"><span data-stu-id="7adca-322">Connect the host computer to a power cord before you run guest patching.</span></span>

### <span data-ttu-id="7adca-323">EXPÉRIENCE utilisateur</span><span class="sxs-lookup"><span data-stu-id="7adca-323">Client UX</span></span>

### <span data-ttu-id="7adca-324">ID d’événement 14003</span><span class="sxs-lookup"><span data-stu-id="7adca-324">Event ID 14003</span></span>

<span data-ttu-id="7adca-325">Le message de statut de la barre d’état suivi est trop long et n’a pas pu s’afficher: &lt; *bac \ _status \ _message*&gt;</span><span class="sxs-lookup"><span data-stu-id="7adca-325">The following tray status message was too long and could not be displayed: &lt;*tray\_status\_message*&gt;</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-326">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-326">Description</span></span>**  
<span data-ttu-id="7adca-327">MED-V a créé une chaîne inattendue qui était trop longue pour l’info-bulle de la barre d’État ou le message.</span><span class="sxs-lookup"><span data-stu-id="7adca-327">MED-V created an unanticipated string that was too long for the tray tooltip or balloon message.</span></span> <span data-ttu-id="7adca-328">Le message affiché a donc été tronqué.</span><span class="sxs-lookup"><span data-stu-id="7adca-328">As a result, the displayed message was truncated.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-329">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-329">Solution</span></span>**  
<span data-ttu-id="7adca-330">Il s’agit d’une erreur rares qui peut se produire lorsque MED-V crée de manière aléatoire le texte de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="7adca-330">This is a rare error that can occur when MED-V is randomly creating the tooltip text.</span></span> <span data-ttu-id="7adca-331">Il n’existe aucune solution.</span><span class="sxs-lookup"><span data-stu-id="7adca-331">There is no solution.</span></span>

### <span data-ttu-id="7adca-332">ID d’événement 14004</span><span class="sxs-lookup"><span data-stu-id="7adca-332">Event ID 14004</span></span>

<span data-ttu-id="7adca-333">MED-V arrêté en raison d’une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="7adca-333">MED-V stopped due to an unhandled exception.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-334">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-334">Description</span></span>**  
<span data-ttu-id="7adca-335">Une exception non gérée a entraîné l’arrêt inattendu de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-335">An unhandled exception caused MED-V to stop unexpectedly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-336">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-336">Solution</span></span>**  
<span data-ttu-id="7adca-337">Redémarrez MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-337">Restart MED-V.</span></span>

### <span data-ttu-id="7adca-338">ID d’événement 14005</span><span class="sxs-lookup"><span data-stu-id="7adca-338">Event ID 14005</span></span>

<span data-ttu-id="7adca-339">Le serveur a essayé de créer un mutex, mais il existait déjà.</span><span class="sxs-lookup"><span data-stu-id="7adca-339">Server attempted to create mutex but it already existed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-340">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-340">Description</span></span>**  
<span data-ttu-id="7adca-341">Une deuxième instance de MedvHost.exe est bloquée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="7adca-341">A second instance of MedvHost.exe is stuck in memory.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-342">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-342">Solution</span></span>**  
<span data-ttu-id="7adca-343">Ouvrez TaskManager et mettez fin à tous les processus MedvHost.exe.</span><span class="sxs-lookup"><span data-stu-id="7adca-343">Open TaskManager and end all MedvHost.exe processes.</span></span>

### <span data-ttu-id="7adca-344">ID d’événement 14006</span><span class="sxs-lookup"><span data-stu-id="7adca-344">Event ID 14006</span></span>

<span data-ttu-id="7adca-345">Erreur lors de la modification ou de la suppression de la valeur du Registre &lt; *\ _Value* &gt; .</span><span class="sxs-lookup"><span data-stu-id="7adca-345">Error modifying or deleting registry value &lt;*registry\_value*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-346">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-346">Description</span></span>**  
<span data-ttu-id="7adca-347">MED-V ne peut pas modifier l’entrée spécifiée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7adca-347">MED-V is unable to modify the specified entry in the registry.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-348">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-348">Solution</span></span>**  
<span data-ttu-id="7adca-349">Vérifiez que vous avez installé ou désinstallé MED-V avec les informations d’identification d’administration.</span><span class="sxs-lookup"><span data-stu-id="7adca-349">Ensure that you install or uninstall MED-V with administrative credentials.</span></span>

### <span data-ttu-id="7adca-350">ID d’événement 14007</span><span class="sxs-lookup"><span data-stu-id="7adca-350">Event ID 14007</span></span>

<span data-ttu-id="7adca-351">Le fichier spécifié ( &lt; *nom*de fichier &gt; ) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7adca-351">The file specified (&lt;*filename*&gt;) is not valid.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-352">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-352">Description</span></span>**  
<span data-ttu-id="7adca-353">Lors de l’installation ou de la désinstallation, un fichier temporaire endommagé a été transmis à l’hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-353">During install or uninstall, a corrupted temp file was passed to MED-V host.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-354">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-354">Solution</span></span>**  
<span data-ttu-id="7adca-355">Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-355">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="7adca-356">ID d’événement 14008</span><span class="sxs-lookup"><span data-stu-id="7adca-356">Event ID 14008</span></span>

<span data-ttu-id="7adca-357">Fichier introuvable: nom de fichier &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="7adca-357">File not found: &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-358">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-358">Description</span></span>**  
<span data-ttu-id="7adca-359">Lors de l’installation ou de la désinstallation, le chemin d’accès d’un fichier temporaire requis est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7adca-359">During install or uninstall, a path of a required temp file was not found.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-360">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-360">Solution</span></span>**  
<span data-ttu-id="7adca-361">Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-361">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="7adca-362">ID d’événement 14009</span><span class="sxs-lookup"><span data-stu-id="7adca-362">Event ID 14009</span></span>

<span data-ttu-id="7adca-363">Impossible de lire le fichier de paramètres &lt; *nom_fichier* &gt; .</span><span class="sxs-lookup"><span data-stu-id="7adca-363">Unable to read parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-364">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-364">Description</span></span>**  
<span data-ttu-id="7adca-365">Pendant le processus d’installation ou de désinstallation, MED-V n’a pas pu lire un fichier temporaire.</span><span class="sxs-lookup"><span data-stu-id="7adca-365">During the install or uninstall process, MED-V was unable to read a temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-366">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-366">Solution</span></span>**  
<span data-ttu-id="7adca-367">Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-367">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="7adca-368">Par ailleurs, vérifiez que l’utilisateur dispose des droits et autorisations nécessaires sur le dossier Temp.</span><span class="sxs-lookup"><span data-stu-id="7adca-368">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="7adca-369">ID d’événement 14010</span><span class="sxs-lookup"><span data-stu-id="7adca-369">Event ID 14010</span></span>

<span data-ttu-id="7adca-370">Erreur de fichier de paramètre de désérialisation &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="7adca-370">Error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-371">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-371">Description</span></span>**  
<span data-ttu-id="7adca-372">Pendant le processus d’installation ou de désinstallation, MED-V a détecté un fichier temporaire endommagé.</span><span class="sxs-lookup"><span data-stu-id="7adca-372">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-373">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-373">Solution</span></span>**  
<span data-ttu-id="7adca-374">Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-374">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="7adca-375">Par ailleurs, vérifiez que l’utilisateur dispose des droits et autorisations nécessaires sur le dossier Temp.</span><span class="sxs-lookup"><span data-stu-id="7adca-375">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="7adca-376">ID d’événement 14011</span><span class="sxs-lookup"><span data-stu-id="7adca-376">Event ID 14011</span></span>

<span data-ttu-id="7adca-377">Erreur inattendue lors de la désérialisation &lt; *du nom*de fichier du paramètre &gt; .</span><span class="sxs-lookup"><span data-stu-id="7adca-377">Unexpected error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-378">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-378">Description</span></span>**  
<span data-ttu-id="7adca-379">Pendant le processus d’installation ou de désinstallation, MED-V a détecté un fichier temporaire endommagé.</span><span class="sxs-lookup"><span data-stu-id="7adca-379">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-380">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-380">Solution</span></span>**  
<span data-ttu-id="7adca-381">Supprimez tous les fichiers dans le dossier Temp, puis réinstallez ou désinstallez MED-V.</span><span class="sxs-lookup"><span data-stu-id="7adca-381">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="7adca-382">Par ailleurs, vérifiez que l’utilisateur dispose des droits et autorisations nécessaires sur le dossier Temp.</span><span class="sxs-lookup"><span data-stu-id="7adca-382">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="7adca-383">ID d’événement 14012</span><span class="sxs-lookup"><span data-stu-id="7adca-383">Event ID 14012</span></span>

<span data-ttu-id="7adca-384">Erreur inattendue lors de l’utilisation des droits de paramètres sur le &lt; *dossier de dossiers \ _name* &gt; pour &lt; *nom d'* utilisateur &gt; .</span><span class="sxs-lookup"><span data-stu-id="7adca-384">Unexpected error when settings rights on folder &lt;*folder\_name*&gt; for user &lt;*username*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-385">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-385">Description</span></span>**  
<span data-ttu-id="7adca-386">Une erreur se produit lorsque MED-V est incapable de définir des droits et des autorisations sur certains dossiers lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="7adca-386">An error occurs when MED-V is unable to set rights and permissions on certain folders during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-387">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-387">Solution</span></span>**  
<span data-ttu-id="7adca-388">Activez les droits d’administrateur pour les dossiers suivants:</span><span class="sxs-lookup"><span data-stu-id="7adca-388">Check the administrator rights to the following folders:</span></span>

<span data-ttu-id="7adca-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span><span class="sxs-lookup"><span data-stu-id="7adca-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span></span>

<span data-ttu-id="7adca-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span><span class="sxs-lookup"><span data-stu-id="7adca-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span></span>

<span data-ttu-id="7adca-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span><span class="sxs-lookup"><span data-stu-id="7adca-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span></span>

### <span data-ttu-id="7adca-392">ID d’événement 14013</span><span class="sxs-lookup"><span data-stu-id="7adca-392">Event ID 14013</span></span>

<span data-ttu-id="7adca-393">Erreur inattendue lors de la création d’un fichier verrouillé.</span><span class="sxs-lookup"><span data-stu-id="7adca-393">Unexpected error when creating lock file.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="7adca-394">Description</span><span class="sxs-lookup"><span data-stu-id="7adca-394">Description</span></span>**  
<span data-ttu-id="7adca-395">Une erreur se produit lorsque MED-V ne peut pas créer de fichier dans le dossier @ «%ProgramData%\\Microsoft\\Medv\\MedvLock» lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="7adca-395">An error occurs when MED-V is unable to create a file in the @"%ProgramData%\\Microsoft\\Medv\\MedvLock" folder during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="7adca-396">Solution</span><span class="sxs-lookup"><span data-stu-id="7adca-396">Solution</span></span>**  
<span data-ttu-id="7adca-397">Vérifiez les droits d’administrateur pour le dossier MedvLock.</span><span class="sxs-lookup"><span data-stu-id="7adca-397">Check the administrator rights to the MedvLock folder.</span></span>

## <span data-ttu-id="7adca-398">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7adca-398">Related topics</span></span>


[<span data-ttu-id="7adca-399">Résolution des problèmes liés à MED-V</span><span class="sxs-lookup"><span data-stu-id="7adca-399">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





