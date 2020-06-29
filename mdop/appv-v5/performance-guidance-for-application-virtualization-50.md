---
title: Guide des performances pour Application Virtualization5.0
description: Guide des performances pour Application Virtualization5.0
author: dansimp
ms.assetid: 6b3a3255-b957-4b9b-8bfc-a93fe8438a81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b0f5ef07935fc34adce772e7b2fff85a12b01dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805052"
---
# <span data-ttu-id="614bf-103">Guide des performances pour Application Virtualization5.0</span><span class="sxs-lookup"><span data-stu-id="614bf-103">Performance Guidance for Application Virtualization 5.0</span></span>


<span data-ttu-id="614bf-104">Découvrez comment configurer App-V 5,0 pour obtenir des performances optimales, optimiser les packages d’application virtuelles et offrir une meilleure expérience utilisateur avec les services Bureau à distance et VDI.</span><span class="sxs-lookup"><span data-stu-id="614bf-104">Learn how to configure App-V 5.0 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="614bf-105">L’implémentation de plusieurs méthodes peut vous aider à améliorer l’utilisation de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="614bf-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="614bf-106">Toutefois, votre environnement ne prend pas en charge toutes les méthodes.</span><span class="sxs-lookup"><span data-stu-id="614bf-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="614bf-107">Nous vous conseillons de lire et de comprendre les informations suivantes avant de lire ce document.</span><span class="sxs-lookup"><span data-stu-id="614bf-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="614bf-108">Guide de l’administrateur de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="614bf-108">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="614bf-109">Version de l’application et du client App-V 5 SP2</span><span class="sxs-lookup"><span data-stu-id="614bf-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="614bf-110">Guide de mise en route de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="614bf-110">Microsoft Application Virtualization 5.0 Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="614bf-111">Remarque</span><span class="sxs-lookup"><span data-stu-id="614bf-111">Note</span></span>**  
<span data-ttu-id="614bf-112">Les termes utilisés dans ce document peuvent avoir une signification différente en fonction de la source et du contexte externes.</span><span class="sxs-lookup"><span data-stu-id="614bf-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="614bf-113">Pour plus d’informations sur les conditions d’utilisation de ce document, suivies d’un astérisque **\\** \*, voir la section [terminologie des recommandations](#bkmk-terms1) en matière de performances de la virtualisation d’applications de ce document.</span><span class="sxs-lookup"><span data-stu-id="614bf-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="614bf-114">Enfin, ce document vous fournit les informations nécessaires pour configurer l’ordinateur exécutant le client App-V 5,0 et l’environnement pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="614bf-114">Finally, this document will provide you with the information to configure the computer running App-V 5.0 client and the environment for optimal performance.</span></span> <span data-ttu-id="614bf-115">Optimisez vos packages d’applications virtuelles à des fins de performance à l’aide du Sequencer, et apprenez à utiliser les technologies de gestion de l’expérience utilisateur (UE-V) ou d’autres technologies de gestion de l’environnement utilisateur pour offrir une expérience utilisateur optimale avec App-V 5,0 dans les services Bureau à distance et les infrastructures de bureau virtuelles non persistantes.</span><span class="sxs-lookup"><span data-stu-id="614bf-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.0 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="614bf-116">Pour vous aider à déterminer quelles informations sont pertinentes pour votre environnement, vous devez consulter la liste rapide de chaque section et la liste de contrôle d’applicabilité.</span><span class="sxs-lookup"><span data-stu-id="614bf-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-0-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="614bf-117">App-V 5,0 dans des déploiements sans état persistant</span><span class="sxs-lookup"><span data-stu-id="614bf-117">App-V 5.0 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="614bf-118">Cette section fournit des informations sur une approche permettant de s’assurer que l’utilisateur a accès à toutes les applications virtuelles en quelques secondes après la connexion.</span><span class="sxs-lookup"><span data-stu-id="614bf-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="614bf-119">Pour cela, il suffit de traiter de manière unique l’actualisation de la publication de l’application-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="614bf-119">This is achieved by uniquely addressing the often long-running App-V 5.0 publishing refresh.</span></span> <span data-ttu-id="614bf-120">Comme vous le découvrirez le niveau de base de l’approche, l’actualisation de publication la plus rapide est d’une qui ne doit pas réellement faire quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="614bf-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="614bf-121">Un certain nombre de conditions doivent être respectées et suivre les étapes pour offrir une expérience utilisateur optimale.</span><span class="sxs-lookup"><span data-stu-id="614bf-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="614bf-122">Pour plus d’informations, utilisez les informations fournies dans la section suivante:</span><span class="sxs-lookup"><span data-stu-id="614bf-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="614bf-123">[Scénarios d’utilisation](#bkmk-us) : lorsque vous passez en revue les deux scénarios, gardez à l’esprit qu’il s’agit de l’approche extrême.</span><span class="sxs-lookup"><span data-stu-id="614bf-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="614bf-124">En fonction de vos besoins en matière d’utilisation, vous pouvez choisir d’appliquer ces étapes à un sous-ensemble d’utilisateurs et/ou de packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="614bf-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="614bf-125">Optimisée pour les performances: pour offrir une expérience optimale, vous pouvez vous attendre que l’image de base inclue une partie du package d’application virtuelle App-V.</span><span class="sxs-lookup"><span data-stu-id="614bf-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="614bf-126">Cette configuration est abordée.</span><span class="sxs-lookup"><span data-stu-id="614bf-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="614bf-127">Optimisé pour le stockage: Si vous vous souciez de l’impact sur le stockage, suivez ce scénario pour mieux répondre à ces inquiétudes.</span><span class="sxs-lookup"><span data-stu-id="614bf-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="614bf-128">Préparation de votre environnement</span><span class="sxs-lookup"><span data-stu-id="614bf-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="614bf-129">Étapes à suivre pour préparer l’image de base, que ce soit dans un environnement VDI ou hôte non persistant, seules quelques étapes doivent être effectuées dans l’image de base pour activer cette approche.</span><span class="sxs-lookup"><span data-stu-id="614bf-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="614bf-130">Utiliser UE-V 2,0 comme solution de gestion des profils utilisateur pour l’approche App-V: la pierre angulaire de cette approche est la capacité d’une solution UEM de conserver le contenu de quelques emplacements de Registre et de fichiers.</span><span class="sxs-lookup"><span data-stu-id="614bf-130">Use UE-V 2.0 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="614bf-131">Ces lieux constituent les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="614bf-132">Veillez à consulter la configuration requise pour la solution UPM.</span><span class="sxs-lookup"><span data-stu-id="614bf-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="614bf-133">Utilisation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="614bf-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="614bf-134">Procédure pas à pas: il s’agit d’une procédure pas à pas illustrant les opérations App-V et UE-V ainsi que les attentes des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="614bf-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="614bf-135">Résultat: cette opération décrit les résultats attendus.</span><span class="sxs-lookup"><span data-stu-id="614bf-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="614bf-136">Impact sur le cycle de vie des packages</span><span class="sxs-lookup"><span data-stu-id="614bf-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="614bf-137">Amélioration de l’interface VDI via l’optimisation et l’optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="614bf-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="614bf-138">Liste de vérification d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="614bf-138">Applicability Checklist</span></span>

<span data-ttu-id="614bf-139">Environnement de déploiement</span><span class="sxs-lookup"><span data-stu-id="614bf-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="614bf-140">VDI ou hôte non persistant.</span><span class="sxs-lookup"><span data-stu-id="614bf-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="614bf-141">La virtualisation de l’interface utilisateur (UE-V), les autres solutions UPM ou les disques de profil utilisateur (UPD).</span><span class="sxs-lookup"><span data-stu-id="614bf-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="614bf-142">Configuration prévue</span><span class="sxs-lookup"><span data-stu-id="614bf-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="614bf-143">Virtualisation de l’utilisation des utilisateurs (UE-V) avec le modèle d’état utilisateur App-V activé ou le logiciel de gestion des profils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="614bf-144">Le logiciel de UPM sans UE-V doit être capable de déclencher le déclenchement de la connexion ou du démarrage de processus/application.</span><span class="sxs-lookup"><span data-stu-id="614bf-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="614bf-145">Le magasin de contenus partagés App-V (SCS) est configuré ou peut être configuré.</span><span class="sxs-lookup"><span data-stu-id="614bf-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="614bf-146">Administration informatique</span><span class="sxs-lookup"><span data-stu-id="614bf-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="614bf-147">Il est possible que l’administrateur ait besoin de mettre à jour l’image de base de l’ordinateur virtuel pour garantir des performances optimales ou s’il doit gérer plusieurs images pour différents groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="614bf-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="614bf-148">Scénario d’utilisation</span><span class="sxs-lookup"><span data-stu-id="614bf-148">Usage Scenario</span></span>

<span data-ttu-id="614bf-149">Lorsque vous passez en revue les deux scénarios, gardez à l’esprit que ces deux approches sont extrêmes.</span><span class="sxs-lookup"><span data-stu-id="614bf-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="614bf-150">En fonction de vos besoins en matière d’utilisation, vous pouvez choisir d’appliquer ces étapes à un sous-ensemble d’utilisateurs, des packages d’applications virtuelles ou les deux.</span><span class="sxs-lookup"><span data-stu-id="614bf-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-151">Optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="614bf-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="614bf-152">Optimisé pour le stockage</span><span class="sxs-lookup"><span data-stu-id="614bf-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="614bf-153">Pour fournir une utilisation optimale de l’utilisateur, cette approche exploite les fonctionnalités d’une solution UPM et nécessite une préparation supplémentaire de l’image et peut occasionner une surcharge supplémentaire de gestion des images.</span><span class="sxs-lookup"><span data-stu-id="614bf-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="614bf-154">Ce qui suit décrit de nombreuses améliorations des performances dans les déploiements sans état persistants.</span><span class="sxs-lookup"><span data-stu-id="614bf-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="614bf-155">Pour plus d’informations, reportez-vous <strong> aux étapes de séquençage pour optimiser les packages pour les performances de publication </strong> et la référence au <strong> Guide de séquençage App-V 5,0 </strong> dans la <strong> section Voir aussi de ce document </strong> .</span><span class="sxs-lookup"><span data-stu-id="614bf-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V 5.0 Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-156">Les attentes générales du scénario précédent continuent de s’appliquer ici.</span><span class="sxs-lookup"><span data-stu-id="614bf-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="614bf-157">Néanmoins, gardez à l’esprit que les images VM sont généralement stockées dans des tableaux très coûteux; une légère modification a été apportée à l’approche.</span><span class="sxs-lookup"><span data-stu-id="614bf-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="614bf-158">Ne configurez pas les packages d’application virtuelle ciblés par l’utilisateur dans l’image de base.</span><span class="sxs-lookup"><span data-stu-id="614bf-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="614bf-159">L’impact de cette modification est décrit dans la section démonstration de l’utilisation de l’utilisateur de ce document.</span><span class="sxs-lookup"><span data-stu-id="614bf-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="614bf-160">Préparation de votre environnement</span><span class="sxs-lookup"><span data-stu-id="614bf-160">Preparing your Environment</span></span>

<span data-ttu-id="614bf-161">Le tableau suivant répertorie les étapes nécessaires pour préparer l’image de base et l’UE-V ou une autre solution UPM pour l’approche.</span><span class="sxs-lookup"><span data-stu-id="614bf-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="614bf-162">Préparer l’image de base</span><span class="sxs-lookup"><span data-stu-id="614bf-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-163">Optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="614bf-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="614bf-164">Optimisé pour le stockage</span><span class="sxs-lookup"><span data-stu-id="614bf-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="614bf-165">Installez le package de correctif 4 pour la version cliente du SP2 application de virtualisation d’applications 5,0.</span><span class="sxs-lookup"><span data-stu-id="614bf-165">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="614bf-166">Pour installer UE-V et télécharger le modèle de paramètres App-V à partir de la Galerie de modèles UE-V, voir les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="614bf-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="614bf-167">Configurer pour le mode de magasin de contenus partagés (SCS).</span><span class="sxs-lookup"><span data-stu-id="614bf-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="614bf-168">Pour plus d’informations, reportez-vous <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> à l’installation du client App-V 5,0 pour le mode magasin de contenu partagé </a> .</span><span class="sxs-lookup"><span data-stu-id="614bf-168">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-169">Configurez les intégrations utilisateur dans Registre de connexion DWORD.</span><span class="sxs-lookup"><span data-stu-id="614bf-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="614bf-170">Préconfigurer tous les packages ciblés par l’utilisateur et le niveau global (par exemple, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="614bf-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-171">Préconfigurer tous les groupes de connexions ciblés par l’utilisateur et le niveau global, par exemple, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="614bf-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-172">Publiez préalablement tous les packages destinés au global.</span><span class="sxs-lookup"><span data-stu-id="614bf-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="614bf-173">Vous pouvez également</span><span class="sxs-lookup"><span data-stu-id="614bf-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-174">Effectuer une publication/actualisation globale.</span><span class="sxs-lookup"><span data-stu-id="614bf-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="614bf-175">Effectuer une publication/actualisation utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="614bf-176">Annulez la publication de tous les packages ciblés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="614bf-177">Supprimez les entrées de système de fichiers virtuelles utilisateur (VFS) suivantes.</span><span class="sxs-lookup"><span data-stu-id="614bf-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="614bf-178">Installez le package de correctif 4 pour la version cliente du SP2 application de virtualisation d’applications 5,0.</span><span class="sxs-lookup"><span data-stu-id="614bf-178">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="614bf-179">Pour installer UE-V et télécharger le modèle de paramètres App-V à partir de la Galerie de modèles UE-V, voir les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="614bf-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="614bf-180">Configurer pour le mode de magasin de contenus partagés (SCS).</span><span class="sxs-lookup"><span data-stu-id="614bf-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="614bf-181">Pour plus d’informations, reportez-vous <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> à l’installation du client App-V 5,0 pour le mode magasin de contenu partagé </a> .</span><span class="sxs-lookup"><span data-stu-id="614bf-181">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-182">Configurez les intégrations utilisateur dans Registre de connexion DWORD.</span><span class="sxs-lookup"><span data-stu-id="614bf-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="614bf-183">Préconfigurer tous les packages ciblés globalement par exemple, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="614bf-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-184">Configurez tous les groupes de connexions cibles globales, par exemple, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="614bf-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-185">Publiez préalablement tous les packages destinés au global.</span><span class="sxs-lookup"><span data-stu-id="614bf-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="614bf-186">**Configurations** -pour les configurations de client d’application V critiques et pour un peu plus de contexte et de procédure, consultez les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="614bf-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-187">Paramètre de configuration</span><span class="sxs-lookup"><span data-stu-id="614bf-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="614bf-188">Qu’est-ce que c’est?</span><span class="sxs-lookup"><span data-stu-id="614bf-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="614bf-189">Comment dois-je l’utiliser?</span><span class="sxs-lookup"><span data-stu-id="614bf-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="614bf-190">Mode de magasin de contenus partagés (SCS)</span><span class="sxs-lookup"><span data-stu-id="614bf-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-191">Configurable dans PowerShell à l’aide de <strong> Set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> ou</span><span class="sxs-lookup"><span data-stu-id="614bf-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="614bf-192">Lors de l’installation du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="614bf-192">During installation of the App-V 5.0 client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="614bf-193">Lors de l’exécution du magasin de contenu partagé, seules les données de publication sont conservées sur le disque dur; les autres ressources d’application virtuelles sont conservées en mémoire (RAM).</span><span class="sxs-lookup"><span data-stu-id="614bf-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="614bf-194">Cela permet de conserver le stockage local et de réduire les e/s de disque par seconde (IOPS).</span><span class="sxs-lookup"><span data-stu-id="614bf-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-195">Cette option est recommandée lorsque les connexions à faible latence sont disponibles entre le point de terminaison du client App-V et le serveur de contenu SCS.</span><span class="sxs-lookup"><span data-stu-id="614bf-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="614bf-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="614bf-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-197">Configurer dans le Registre sous <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> </strong>  \  <strong> intégration du </strong>  \  <strong> client Microsoft AppV </strong>  \  <strong> </strong>  \  <strong> </strong> du logiciel.</span><span class="sxs-lookup"><span data-stu-id="614bf-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-198">Créez la valeur DWORD <strong> PreserveUserIntegrationsOnLogin </strong> avec la valeur <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="614bf-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-199">Redémarrez le service client App-V ou redémarrez l’ordinateur exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="614bf-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="614bf-200">Si vous n’avez pas encore préconfiguré ( <strong> Add-AppvClientPackage </strong> ) d’un package spécifique et que ce paramètre n’est pas configuré, le client App-V va de nouveau intégrer \* les intégrations utilisateur persistantes, puis réintégrer \*.</span><span class="sxs-lookup"><span data-stu-id="614bf-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="614bf-201">Pour tous les packages qui remplissent les conditions ci-dessus, il est plus efficace de procéder au travail lors de la publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="614bf-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-202">Si vous envisagez de préconfigurer tous les packages d’utilisateurs disponibles dans l’image de base, utilisez ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="614bf-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="614bf-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="614bf-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-204">Configurez le registre dans le Registre sous HKEY_LOCAL_MACHINE publications puissantes du <strong> </strong> &lt; &gt; </strong>  \  <strong> </strong>  \  <strong> client Microsoft AppV </strong> &lt; &gt; </strong>  \  <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="614bf-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="614bf-205">Créez la valeur DWORD <strong> MaxConcurrentPublishingrefresh </strong> en utilisant le nombre maximal de rafraîchissements simultanés de la publication.</span><span class="sxs-lookup"><span data-stu-id="614bf-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="614bf-206">Il n’est pas nécessaire de relancer le service client et l’ordinateur App-V.</span><span class="sxs-lookup"><span data-stu-id="614bf-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="614bf-207">Ce paramètre détermine le nombre d’utilisateurs qui peuvent effectuer une actualisation ou une synchronisation de publication en même temps.</span><span class="sxs-lookup"><span data-stu-id="614bf-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="614bf-208">Le paramètre par défaut est sans limite.</span><span class="sxs-lookup"><span data-stu-id="614bf-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-209">Limiter le nombre de rafraîchissements de publication simultanées évite une utilisation excessive de l’UC qui peut affecter les performances de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="614bf-210">Cette limite est recommandée dans un environnement RDS, où plusieurs utilisateurs peuvent se connecter au même ordinateur en même temps et effectuer une synchronisation d’actualisation de publication.</span><span class="sxs-lookup"><span data-stu-id="614bf-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="614bf-211">Si le seuil d’actualisation de publication simultanée est atteint, le temps requis pour publier de nouvelles applications et les mettre à la disposition des utilisateurs finaux après leur connexion peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="614bf-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="614bf-212">Configurer une solution UE-V pour l’approche App-v</span><span class="sxs-lookup"><span data-stu-id="614bf-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="614bf-213">Nous vous recommandons d’utiliser la virtualisation de l’utilisation de Microsoft User (UE-V) pour capturer et centraliser les paramètres d’application et les paramètres du système d’exploitation Windows pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="614bf-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="614bf-214">Ces paramètres sont ensuite appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="614bf-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="614bf-215">UE-V est optimisée pour les scénarios RDS et VDI.</span><span class="sxs-lookup"><span data-stu-id="614bf-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="614bf-216">Pour plus d’informations, reportez-vous [à la rubrique mise en route de l’interface utilisateur-virtualisation 2,0](https://technet.microsoft.com/library/dn458936.aspx)</span><span class="sxs-lookup"><span data-stu-id="614bf-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458936.aspx)</span></span>

<span data-ttu-id="614bf-217">Par essence, il est nécessaire d’installer le client UE-V et de télécharger le modèle de paramètres App-v Microsoft créé à partir de la [Galerie de modèles Microsoft User Interface (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span><span class="sxs-lookup"><span data-stu-id="614bf-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="614bf-218">Enregistrez le modèle.</span><span class="sxs-lookup"><span data-stu-id="614bf-218">Register the template.</span></span> <span data-ttu-id="614bf-219">Pour plus d’informations sur les modèles UE-V, voir [la ressource spécifique d’UE-v pour l’acquisition et l’inscription du modèle](https://technet.microsoft.com/library/dn458936.aspx).</span><span class="sxs-lookup"><span data-stu-id="614bf-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458936.aspx).</span></span>

**<span data-ttu-id="614bf-220">Remarque</span><span class="sxs-lookup"><span data-stu-id="614bf-220">Note</span></span>**  
<span data-ttu-id="614bf-221">Sans exécuter une étape de configuration supplémentaire, la virtualisation de l’environnement utilisateur Microsoft (UE-V) ne sera pas en mesure de synchroniser les raccourcis du menu Démarrer (fichiers. lnk) sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="614bf-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="614bf-222">Le type de fichier. lnk est exclu par défaut.</span><span class="sxs-lookup"><span data-stu-id="614bf-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="614bf-223">UE-V ne prend en charge que la suppression du type de fichier. lnk de la liste d’exclusions dans les scénarios RDS et VDI, où l’appareil de chaque utilisateur dispose du même ensemble d’applications installées sur le même emplacement et chaque fichier. lnk est valide pour tous les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="614bf-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="614bf-224">Par exemple, UE-V ne prend pas en charge les 2 scénarios suivants, car le résultat net sera valide sur un seul, mais pas sur tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="614bf-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="614bf-225">Si un utilisateur dispose d’une application installée sur un appareil avec fichiers. lnk activés et de la même application native installée sur un autre appareil à une autre racine d’installation avec les fichiers. lnk activés.</span><span class="sxs-lookup"><span data-stu-id="614bf-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="614bf-226">Si un utilisateur a installé une application sur un appareil, mais pas un autre avec des fichiers. lnk activés.</span><span class="sxs-lookup"><span data-stu-id="614bf-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="614bf-227">Important</span><span class="sxs-lookup"><span data-stu-id="614bf-227">Important</span></span>**  
<span data-ttu-id="614bf-228">Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="614bf-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="614bf-229">Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows.</span><span class="sxs-lookup"><span data-stu-id="614bf-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="614bf-230">Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre.</span><span class="sxs-lookup"><span data-stu-id="614bf-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="614bf-231">Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="614bf-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="614bf-232">Changez de Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="614bf-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="614bf-233">À l’aide de l’éditeur du Registre Microsoft (regedit.exe), accédez à la section **HKEY \ _LOCAL \ _MACHINE**  \\  **logiciel**  \\  **Microsoft**  \\  **UEV**  \\  **agent**  \\  **configuration**  \\  **ExcludedFileTypes** et supprimez le fichier **. lnk** des types de fichiers exclus.</span><span class="sxs-lookup"><span data-stu-id="614bf-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="614bf-234">Configurer une solution de gestion des profils utilisateur pour l’application-V</span><span class="sxs-lookup"><span data-stu-id="614bf-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="614bf-235">L’attente dans un environnement avec état est qu’une solution UPM est implémentée et peut prendre en charge la persistance des données utilisateur entre des sessions et entre des connexions.</span><span class="sxs-lookup"><span data-stu-id="614bf-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="614bf-236">La configuration requise pour la solution UPM est la suivante:</span><span class="sxs-lookup"><span data-stu-id="614bf-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="614bf-237">Pour garantir une expérience de connexion optimisée (par exemple, l’approche App-V 5,0 pour l’utilisateur), la solution doit être capable de:</span><span class="sxs-lookup"><span data-stu-id="614bf-237">To enable an optimized login experience, for example the App-V 5.0 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="614bf-238">La conservation des intégrations utilisateur dans le cadre du profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="614bf-239">Le déclenchement d’une synchronisation de profil utilisateur à l’ouverture de session (ou de début de l’application), qui peut garantir l’application de toutes les intégrations utilisateur avant le début de la publication/actualisation; ou</span><span class="sxs-lookup"><span data-stu-id="614bf-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="614bf-240">Attachement et détachement d’un disque de profil utilisateur ou d’une technologie similaire contenant les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

-   <span data-ttu-id="614bf-241">Capture des modifications apportées aux emplacements, qui constituent les intégrations utilisateur, avant la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="614bf-241">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="614bf-242">Avec App-V 5,0 lorsque vous ajoutez un serveur de publication (**Add-AppvPublishingServer**), vous pouvez configurer la synchronisation, par exemple pour l’actualisation lors de la connexion et/ou après un intervalle d’actualisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="614bf-242">With App-V 5.0 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="614bf-243">Dans les deux cas, une tâche planifiée est créée.</span><span class="sxs-lookup"><span data-stu-id="614bf-243">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="614bf-244">Dans les versions précédentes de App-V 5,0, les deux tâches planifiées ont été configurées à l’aide d’un code VBScript qui initierait l’actualisation globale et de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-244">In previous versions of App-V 5.0, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="614bf-245">Avec le correctif logiciel 4 pour l’application virtualisation de l’application 5,0 SP2, l’actualisation de l’utilisateur lors de l’ouverture de session est initiée par **SyncAppvPublishingServer.exe**.</span><span class="sxs-lookup"><span data-stu-id="614bf-245">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on is initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="614bf-246">Cette modification a été apportée de manière à fournir des solutions UPM comme processus de déclenchement.</span><span class="sxs-lookup"><span data-stu-id="614bf-246">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="614bf-247">Ce processus va retarder la publication de/Refresh pour permettre à la solution UPM d’appliquer les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-247">This process will delay the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="614bf-248">Elle se fermera une fois que la publication/actualisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="614bf-248">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="614bf-249">Intégrations utilisateur</span><span class="sxs-lookup"><span data-stu-id="614bf-249">User Integrations</span></span>**

<span data-ttu-id="614bf-250">Registry-HKEY \ _CURRENT \ _USER</span><span class="sxs-lookup"><span data-stu-id="614bf-250">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="614bf-251">Path-Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="614bf-251">Path - Software\\Classes</span></span>

    <span data-ttu-id="614bf-252">Exclude: Local Settings, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="614bf-252">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="614bf-253">Path-Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="614bf-253">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="614bf-254">Chemins d’accès-Software\\Microsoft\\Windows\\CurrentVersion\\App</span><span class="sxs-lookup"><span data-stu-id="614bf-254">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="614bf-255">Emplacement des fichiers</span><span class="sxs-lookup"><span data-stu-id="614bf-255">File Locations</span></span>**

-   <span data-ttu-id="614bf-256">Root – «variable d’environnement» APPDATA</span><span class="sxs-lookup"><span data-stu-id="614bf-256">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="614bf-257">Path – Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="614bf-257">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="614bf-258">Root – «variable d’environnement» APPDATA</span><span class="sxs-lookup"><span data-stu-id="614bf-258">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="614bf-259">Path – Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="614bf-259">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="614bf-260">Root – «variable d’environnement» APPDATA</span><span class="sxs-lookup"><span data-stu-id="614bf-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="614bf-261">Path-Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="614bf-261">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="614bf-262">(Pour conserver tous les raccourcis bureau, virtuels et non virtuels)</span><span class="sxs-lookup"><span data-stu-id="614bf-262">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="614bf-263">Root-«KnownFolder» {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ \*. lnk</span><span class="sxs-lookup"><span data-stu-id="614bf-263">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="614bf-264">Virtualisation de l’utilisation de Microsoft User (UE-V)</span><span class="sxs-lookup"><span data-stu-id="614bf-264">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="614bf-265">Par ailleurs, nous vous conseillons d’utiliser Microsoft User Interface Virtualization (UE-V) pour capturer et centraliser les paramètres d’application et les paramètres du système d’exploitation Windows pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="614bf-265">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="614bf-266">Ces paramètres sont ensuite appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="614bf-266">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="614bf-267">Pour plus d’informations, reportez-vous à la rubrique [mise en route de l’utilisation de l’interface utilisateur 1,0](https://technet.microsoft.com/library/jj680015.aspx) et [partage de modèles d’emplacement des paramètres avec la Galerie de modèles UE-V](https://technet.microsoft.com/library/jj679972.aspx).</span><span class="sxs-lookup"><span data-stu-id="614bf-267">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="614bf-268">Utilisation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="614bf-268">User Experience Walk-through</span></span>

<span data-ttu-id="614bf-269">Vous trouverez ci-dessous une procédure pas à pas illustrant les opérations d’application-V et de UPM, ainsi que les attentes des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="614bf-269">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-270">Optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="614bf-270">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="614bf-271">Optimisé pour le stockage</span><span class="sxs-lookup"><span data-stu-id="614bf-271">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="614bf-272">Après l’implémentation de cette approche dans l’environnement VDI/hôte de connexion à la première connexion,</span><span class="sxs-lookup"><span data-stu-id="614bf-272">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-273">Activité Un utilisateur-publication/actualisation est lancé.</span><span class="sxs-lookup"><span data-stu-id="614bf-273">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="614bf-274">Attente S’il s’agit de la première fois qu’un utilisateur a publié des applications virtuelles (par exemple, non persistant), la durée de publication et de rafraîchissement est normale.</span><span class="sxs-lookup"><span data-stu-id="614bf-274">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="614bf-275">Activité Après la publication et l’actualisation, la solution UPM capture les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-275">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="614bf-276">Attente En fonction de la configuration de la solution UPM, cela peut se produire dans le cadre du processus de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="614bf-276">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="614bf-277">Cette opération entraîne la conservation de l’état utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-277">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="614bf-278">Sur les connexions suivantes:</span><span class="sxs-lookup"><span data-stu-id="614bf-278">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-279">Activité La solution UPM applique les intégrations utilisateur au système avant la publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="614bf-279">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="614bf-280">Attente Des raccourcis apparaissent sur votre ordinateur de bureau, ou dans le menu Démarrer, qui fonctionne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="614bf-280">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="614bf-281">Lorsque la publication ou l’actualisation est terminée (par exemple, le changement de package), certains risquent de ne pas être déplacés.</span><span class="sxs-lookup"><span data-stu-id="614bf-281">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="614bf-282">Activité Le processus de publication/actualisation traitera les opérations d’annulation de publication et de publication des modifications apportées aux habilitations du package utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-282">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="614bf-283">Attente S’il n’y a aucune modification d’habilitation, publishing1 se termine en quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="614bf-283">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="614bf-284">Dans le cas contraire, le nombre et la complexité de la publication et de la mise à jour des applications virtuelles seront augmentés.</span><span class="sxs-lookup"><span data-stu-id="614bf-284">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="614bf-285">Activité La solution UPM répartira les intégrations des utilisateurs lors de la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="614bf-285">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="614bf-286">Attente Comme précédent.</span><span class="sxs-lookup"><span data-stu-id="614bf-286">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="614bf-287">¹ l’opération de publication ( <strong> publication-AppVClientPackage </strong> ) ajoute des entrées au catalogue de l’utilisateur, des cartes de habilitation pour l’utilisateur, identifie le magasin local et se termine en effectuant les étapes d’intégration.</span><span class="sxs-lookup"><span data-stu-id="614bf-287">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-288">Après l’implémentation de cette approche dans l’environnement VDI/hôte de connexion à la première connexion,</span><span class="sxs-lookup"><span data-stu-id="614bf-288">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-289">Activité Un utilisateur-publication/actualisation est lancé.</span><span class="sxs-lookup"><span data-stu-id="614bf-289">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="614bf-290">Attente</span><span class="sxs-lookup"><span data-stu-id="614bf-290">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-291">S’il s’agit de la première fois qu’un utilisateur a publié des applications virtuelles (par exemple, non persistant), cette méthode prend la durée habituelle d’une publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="614bf-291">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="614bf-292">Les connexions préalables et suivantes seront affectées en préconfigurant les packages (Ajouter/actualiser).</span><span class="sxs-lookup"><span data-stu-id="614bf-292">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="614bf-293">Activité Après la publication et l’actualisation, la solution UPM capture les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-293">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="614bf-294">Attente En fonction de la configuration de la solution UPM, cela peut se produire dans le cadre du processus de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="614bf-294">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="614bf-295">Cela entraînera la même surcharge ou une surcharge similaire à la conservation de l’état utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-295">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="614bf-296">Sur les connexions suivantes:</span><span class="sxs-lookup"><span data-stu-id="614bf-296">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-297">Activité La solution UPM applique les intégrations utilisateur au système avant la publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="614bf-297">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="614bf-298">Activité L’ajout/actualisation doit préconfigurer toutes les applications ciblées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-298">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="614bf-299">Attente</span><span class="sxs-lookup"><span data-stu-id="614bf-299">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-300">Cela peut ralentir considérablement la disponibilité des applications (selon une période de 10 secondes).</span><span class="sxs-lookup"><span data-stu-id="614bf-300">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="614bf-301">Cela augmente l’heure d’actualisation de publication par rapport au nombre et à la complexité \* des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="614bf-301">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="614bf-302">Activité La publication et l’actualisation traitent les opérations d’annulation de la publication et de publication des modifications apportées aux habilitations du package d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-302">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-303">About</span><span class="sxs-lookup"><span data-stu-id="614bf-303">Outcome</span></span></th>
<th align="left"><span data-ttu-id="614bf-304">About</span><span class="sxs-lookup"><span data-stu-id="614bf-304">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="614bf-305">Dans la mesure où les intégrations utilisateur sont entièrement préservées, il n’y a pas de tâche, par exemple, l’intégration de l’opération de publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="614bf-305">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="614bf-306">Toutes les applications virtuelles seront disponibles en quelques secondes de connexion.</span><span class="sxs-lookup"><span data-stu-id="614bf-306">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="614bf-307">La publication/actualisation traite les modifications apportées aux utilisateurs ayant des applications virtuelles qui ont une incidence sur l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-307">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="614bf-308">Dans la mesure où l’ajout/actualisation doit reconfigurer toutes les applications virtuelles sur la machine virtuelle, le délai d’actualisation de publication sur chaque connexion sera prolongé.</span><span class="sxs-lookup"><span data-stu-id="614bf-308">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="614bf-309">Impact sur le cycle de vie d’un package</span><span class="sxs-lookup"><span data-stu-id="614bf-309">Impact to Package Life Cycle</span></span>

<span data-ttu-id="614bf-310">La mise à niveau d’un package est un aspect essentiel du cycle de vie du package.</span><span class="sxs-lookup"><span data-stu-id="614bf-310">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="614bf-311">Pour garantir que les utilisateurs ont accès aux packages d’applications virtuelles mis à niveau appropriés (publiés) ou mis à niveau (non publié), il est recommandé de mettre à jour l’image de base pour refléter ces modifications.</span><span class="sxs-lookup"><span data-stu-id="614bf-311">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="614bf-312">Pour mieux comprendre pourquoi examinez la section suivante:</span><span class="sxs-lookup"><span data-stu-id="614bf-312">To understand why review the following section:</span></span>

<span data-ttu-id="614bf-313">App-V 5,0 SP2 a instauré le concept d’États en attente.</span><span class="sxs-lookup"><span data-stu-id="614bf-313">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="614bf-314">Par le passé,</span><span class="sxs-lookup"><span data-stu-id="614bf-314">In the past,</span></span>

-   <span data-ttu-id="614bf-315">Si un administrateur a changé d’habilitation ou a créé une nouvelle version d’un package (mise à niveau) et, au cours d’une publication/actualisation, le package était en cours d’utilisation, l’opération d’annulation de publication</span><span class="sxs-lookup"><span data-stu-id="614bf-315">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="614bf-316">À présent, si un package est en cours d’utilisation, l’opération est en attente.</span><span class="sxs-lookup"><span data-stu-id="614bf-316">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="614bf-317">Les opérations d’annulation de publication et de publication en attente seront traitées lors du redémarrage du service ou si une autre commande publier ou annuler la publication est émise.</span><span class="sxs-lookup"><span data-stu-id="614bf-317">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="614bf-318">Dans ce dernier cas, si l’application virtuelle est en cours d’utilisation, l’application virtuelle reste dans un état d’attente.</span><span class="sxs-lookup"><span data-stu-id="614bf-318">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="614bf-319">Pour les packages publiés globalement, un redémarrage (ou un redémarrage du service) est souvent nécessaire.</span><span class="sxs-lookup"><span data-stu-id="614bf-319">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="614bf-320">Dans un environnement non persistant, il est peu probable que les opérations en attente soient traitées.</span><span class="sxs-lookup"><span data-stu-id="614bf-320">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="614bf-321">Les opérations en attente, par exemple les tâches sont capturées sous **HKEY \ _CURRENT \ _USER**  \\  **logiciel**  \\  **Microsoft**  \\  **AppV**  \\  **client**  \\  **PendingTasks**.</span><span class="sxs-lookup"><span data-stu-id="614bf-321">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="614bf-322">Même si cet emplacement est persistant par la solution UPM, si elle n’est pas appliquée à l’environnement avant de se connecter, ce dernier ne sera pas traité.</span><span class="sxs-lookup"><span data-stu-id="614bf-322">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="614bf-323">Amélioration de l’interface VDI par le biais de l’optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="614bf-323">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="614bf-324">La section suivante contient des listes contenant des informations sur les documents et les téléchargements Microsoft qui pourraient s’avérer utiles lors de l’optimisation de votre environnement en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="614bf-324">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="614bf-325">Blog et script .NET NGEN (vivement recommandé)</span><span class="sxs-lookup"><span data-stu-id="614bf-325">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="614bf-326">À propos de la technologie NGEN</span><span class="sxs-lookup"><span data-stu-id="614bf-326">About NGEN technology</span></span>

-   [<span data-ttu-id="614bf-327">Comment accélérer l’optimisation de NGEN</span><span class="sxs-lookup"><span data-stu-id="614bf-327">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="614bf-328">Script</span><span class="sxs-lookup"><span data-stu-id="614bf-328">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="614bf-329">Rôles serveur et serveur Windows</span><span class="sxs-lookup"><span data-stu-id="614bf-329">Windows Server and Server Roles</span></span>**

<span data-ttu-id="614bf-330">Recommandations en matière d’optimisation des performances du serveur pour</span><span class="sxs-lookup"><span data-stu-id="614bf-330">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="614bf-331">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="614bf-331">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="614bf-332">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="614bf-332">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="614bf-333">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="614bf-333">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="614bf-334">Rôles de serveur</span><span class="sxs-lookup"><span data-stu-id="614bf-334">Server Roles</span></span>**

-   [<span data-ttu-id="614bf-335">Hôte de virtualisation du Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="614bf-335">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="614bf-336">Hôte de session Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="614bf-336">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="614bf-337">Pertinence IIS: gestion d’App-V, publication, création de rapports Web services</span><span class="sxs-lookup"><span data-stu-id="614bf-337">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="614bf-338">Pertinence du serveur de fichiers (SMB): s’il est utilisé pour le stockage et la remise des contenus App-V dans le mode SCS</span><span class="sxs-lookup"><span data-stu-id="614bf-338">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="614bf-339">Recommandations en matière d’optimisation des performances de client Windows (système d’exploitation invité)</span><span class="sxs-lookup"><span data-stu-id="614bf-339">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="614bf-340">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="614bf-340">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="614bf-341">Script d’optimisation: (fourni par le support Microsoft)</span><span class="sxs-lookup"><span data-stu-id="614bf-341">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="614bf-342">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="614bf-342">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="614bf-343">Script d’optimisation: (fourni par le support Microsoft)</span><span class="sxs-lookup"><span data-stu-id="614bf-343">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="614bf-344">Étapes de séquençage pour optimiser les packages de performance de publication</span><span class="sxs-lookup"><span data-stu-id="614bf-344">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="614bf-345">App-V 5,0 et App-V 5,0 SP2 fournissent une valeur importante dans leurs versions respectives.</span><span class="sxs-lookup"><span data-stu-id="614bf-345">App-V 5.0 and App-V 5.0 SP2 provide significant value in their respective releases.</span></span> <span data-ttu-id="614bf-346">Plusieurs fonctionnalités simplifient le développement de nouveaux scénarios ou permettent de nouvelles situations de déploiement de clients.</span><span class="sxs-lookup"><span data-stu-id="614bf-346">Several features facilitate new scenarios or enabled new customer deployment scenarios.</span></span> <span data-ttu-id="614bf-347">Les fonctionnalités suivantes peuvent avoir un impact sur les performances des opérations de publication et de lancement.</span><span class="sxs-lookup"><span data-stu-id="614bf-347">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-348">Étape</span><span class="sxs-lookup"><span data-stu-id="614bf-348">Step</span></span></th>
<th align="left"><span data-ttu-id="614bf-349">Facteur</span><span class="sxs-lookup"><span data-stu-id="614bf-349">Consideration</span></span></th>
<th align="left"><span data-ttu-id="614bf-350">Avantages</span><span class="sxs-lookup"><span data-stu-id="614bf-350">Benefits</span></span></th>
<th align="left"><span data-ttu-id="614bf-351">Compromis</span><span class="sxs-lookup"><span data-stu-id="614bf-351">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="614bf-352">Aucun bloc de fonctionnalité 1 (FB1, également connu sous le nom de FB-principal)</span><span class="sxs-lookup"><span data-stu-id="614bf-352">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-353">Non FB1 indique que l’application sera lancée immédiatement et qu’elle nécessite une erreur de type fichier (l’application nécessite un fichier, une DLL et qu’elle doit descendre sur le réseau) lors du lancement. S’il existe des limitations réseau, FB1:</span><span class="sxs-lookup"><span data-stu-id="614bf-353">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="614bf-354">Réduisez le nombre de pannes de flux et de bande passante réseau utilisées lorsque vous lancez une application pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="614bf-354">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="614bf-355">Retardez le lancement jusqu’à ce que la totalité du FB1 ait été diffusée.</span><span class="sxs-lookup"><span data-stu-id="614bf-355">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="614bf-356">Le dysfonctionnement du flux réduit le temps de démarrage.</span><span class="sxs-lookup"><span data-stu-id="614bf-356">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-357">Les packages d’application virtuelle pour lesquels FB1 est configuré doivent être à nouveau séquencés.</span><span class="sxs-lookup"><span data-stu-id="614bf-357">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="614bf-358">Suppression de FB1</span><span class="sxs-lookup"><span data-stu-id="614bf-358">Removing FB1</span></span>

<span data-ttu-id="614bf-359">La suppression de FB1 ne nécessite pas le programme d’installation d’application d’origine.</span><span class="sxs-lookup"><span data-stu-id="614bf-359">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="614bf-360">Après avoir suivi les étapes ci-dessous, il est recommandé de rétablir l’ordinateur qui exécute le Sequencer sur une capture instantanée saine.</span><span class="sxs-lookup"><span data-stu-id="614bf-360">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="614bf-361">**Interface utilisateur de Sequencer** -créez un nouveau package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="614bf-361">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="614bf-362">Suivez les étapes de la séquence pour personnaliser- &gt; streaming.</span><span class="sxs-lookup"><span data-stu-id="614bf-362">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="614bf-363">À l’étape de diffusion, ne sélectionnez pas **l’option optimiser le package de déploiement sur un réseau lent ou peu fiable**.</span><span class="sxs-lookup"><span data-stu-id="614bf-363">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="614bf-364">Le cas échéant, passez au **système d’exploitation cible**.</span><span class="sxs-lookup"><span data-stu-id="614bf-364">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="614bf-365">Modifier un package d’application virtuel existant</span><span class="sxs-lookup"><span data-stu-id="614bf-365">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="614bf-366">Effectuez les étapes de séquençage en continu.</span><span class="sxs-lookup"><span data-stu-id="614bf-366">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="614bf-367">Ne sélectionnez pas **l’option optimiser le package de déploiement sur un réseau lent ou non fiable**.</span><span class="sxs-lookup"><span data-stu-id="614bf-367">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="614bf-368">Accédez à **créer un package**.</span><span class="sxs-lookup"><span data-stu-id="614bf-368">Move to **Create Package**.</span></span>

<span data-ttu-id="614bf-369">**PowerShell** -mise à jour d’un package d’application virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="614bf-369">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="614bf-370">Ouvrez une session PowerShell avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="614bf-370">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="614bf-371">Import-module **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="614bf-371">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="614bf-372">**Update-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="614bf-372">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="614bf-373">"C:\\Packages\\MyPackage.appv"-programme d’installation</span><span class="sxs-lookup"><span data-stu-id="614bf-373">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="614bf-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="614bf-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="614bf-375">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="614bf-375">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="614bf-376">Remarque</span><span class="sxs-lookup"><span data-stu-id="614bf-376">Note</span></span>**  
    <span data-ttu-id="614bf-377">Cette applet de commande nécessite un exécutable (. exe) ou un fichier de commandes (. bat).</span><span class="sxs-lookup"><span data-stu-id="614bf-377">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="614bf-378">Vous devez fournir un exécutable vide ou un fichier de commandes.</span><span class="sxs-lookup"><span data-stu-id="614bf-378">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-379">Étape</span><span class="sxs-lookup"><span data-stu-id="614bf-379">Step</span></span></th>
<th align="left"><span data-ttu-id="614bf-380">Concernant</span><span class="sxs-lookup"><span data-stu-id="614bf-380">Considerations</span></span></th>
<th align="left"><span data-ttu-id="614bf-381">Avantages</span><span class="sxs-lookup"><span data-stu-id="614bf-381">Benefits</span></span></th>
<th align="left"><span data-ttu-id="614bf-382">Compromis</span><span class="sxs-lookup"><span data-stu-id="614bf-382">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="614bf-383">Aucune installation SXS lors de la publication</span><span class="sxs-lookup"><span data-stu-id="614bf-383">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-384">Il n’est pas nécessaire de réorganiser les packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="614bf-384">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="614bf-385">Les assemblys SxS peuvent rester dans le package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="614bf-385">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-386">Les dépendances d’assembly SxS ne sont pas installées au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="614bf-386">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-387">Les dépendances d’assemblage SxS doivent être préinstallées.</span><span class="sxs-lookup"><span data-stu-id="614bf-387">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="614bf-388">Création d’un package d’application virtuelle sur le Sequencer</span><span class="sxs-lookup"><span data-stu-id="614bf-388">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="614bf-389">Si, au cours d’une analyse de Sequencer, un assemblage SxS (par exemple, un CV + + Runtime) est installé dans le cadre de l’installation d’une application, l’assemblage SxS est automatiquement détecté et inclus dans le package.</span><span class="sxs-lookup"><span data-stu-id="614bf-389">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="614bf-390">L’administrateur est alors averti et dispose de l’option d’exclusion de l’assembly SxS.</span><span class="sxs-lookup"><span data-stu-id="614bf-390">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="614bf-391">**Côté client**:</span><span class="sxs-lookup"><span data-stu-id="614bf-391">**Client Side**:</span></span>

<span data-ttu-id="614bf-392">Lors de la publication d’un package d’application virtuelle, le client App-V 5,0 SP2 détectera si une dépendance par SxS requise est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="614bf-392">When publishing a virtual application package, the App-V 5.0 SP2 Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="614bf-393">Si la dépendance n’est pas disponible sur l’ordinateur et qu’elle est incluse dans le package, un programme d’installation Windows traditionnel (.\*\* MSI\*\*) l’installation de l’assembly SxS sera lancée.</span><span class="sxs-lookup"><span data-stu-id="614bf-393">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="614bf-394">Comme nous l’avons mentionné précédemment, installez simplement la dépendance sur l’ordinateur exécutant le client pour vérifier que l’installation de Windows Installer (. msi) ne se produit pas.</span><span class="sxs-lookup"><span data-stu-id="614bf-394">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-395">Étape</span><span class="sxs-lookup"><span data-stu-id="614bf-395">Step</span></span></th>
<th align="left"><span data-ttu-id="614bf-396">Concernant</span><span class="sxs-lookup"><span data-stu-id="614bf-396">Considerations</span></span></th>
<th align="left"><span data-ttu-id="614bf-397">Avantages</span><span class="sxs-lookup"><span data-stu-id="614bf-397">Benefits</span></span></th>
<th align="left"><span data-ttu-id="614bf-398">Compromis</span><span class="sxs-lookup"><span data-stu-id="614bf-398">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="614bf-399">Utilisation sélective de fichiers de configuration dynamiques</span><span class="sxs-lookup"><span data-stu-id="614bf-399">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-400">Le client App-V 5,0 doit analyser et traiter les fichiers de configuration dynamique suivants.</span><span class="sxs-lookup"><span data-stu-id="614bf-400">The App-V 5.0 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="614bf-401">Soyez conscient de la taille et de la complexité (exécution du script, inclusions ou exclusions VREG) du fichier.</span><span class="sxs-lookup"><span data-stu-id="614bf-401">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="614bf-402">De nombreux packages d’applications virtuelles peuvent avoir déjà des fichiers de configurations dynamiques spécifiques à un utilisateur ou à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-402">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-403">Les durées de publication sont améliorées si ces fichiers sont utilisés de manière sélective ou pas du tout.</span><span class="sxs-lookup"><span data-stu-id="614bf-403">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-404">Les packages d’applications virtuelles devront être reconfigurés individuellement ou via la console de gestion de l’application-V Server pour supprimer les fichiers de configuration dynamique associés.</span><span class="sxs-lookup"><span data-stu-id="614bf-404">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="614bf-405">Désactivation d’une configuration dynamique à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="614bf-405">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="614bf-406">Pour les packages déjà publiés, vous pouvez utiliser `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` sans</span><span class="sxs-lookup"><span data-stu-id="614bf-406">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="614bf-407">Paramètre **-DynamicDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="614bf-407">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="614bf-408">De même, lorsque vous ajoutez de nouveaux packages à l’aide de `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , n’utilisez pas le</span><span class="sxs-lookup"><span data-stu-id="614bf-408">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="614bf-409">Paramètre **-DynamicDeploymentConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="614bf-409">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="614bf-410">Pour obtenir des informations sur la façon d’appliquer une configuration dynamique, voir:</span><span class="sxs-lookup"><span data-stu-id="614bf-410">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="614bf-411">Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="614bf-411">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

-   [<span data-ttu-id="614bf-412">Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="614bf-412">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="614bf-413">Étape</span><span class="sxs-lookup"><span data-stu-id="614bf-413">Step</span></span></th>
<th align="left"><span data-ttu-id="614bf-414">Concernant</span><span class="sxs-lookup"><span data-stu-id="614bf-414">Considerations</span></span></th>
<th align="left"><span data-ttu-id="614bf-415">Avantages</span><span class="sxs-lookup"><span data-stu-id="614bf-415">Benefits</span></span></th>
<th align="left"><span data-ttu-id="614bf-416">Compromis</span><span class="sxs-lookup"><span data-stu-id="614bf-416">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="614bf-417">Compte d’exécution de script synchrone lors du cycle de vie du package.</span><span class="sxs-lookup"><span data-stu-id="614bf-417">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-418">S’il est incorporé dans le package, l’ajout (PowerShell) peut être considérablement plus lent.</span><span class="sxs-lookup"><span data-stu-id="614bf-418">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="614bf-419">L’exécution de scripts lors du lancement d’une application virtuelle (StartVirtualEnvironment, StartProcess) et/ou ajout + publication aura un impact sur les performances perçues lors d’une ou plusieurs de ces opérations de cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="614bf-419">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-420">L’utilisation de scripts asynchrones (sans blocage) permet de garantir que les opérations de cycle de vie s’exécutent efficacement.</span><span class="sxs-lookup"><span data-stu-id="614bf-420">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-421">Cette étape nécessite une connaissance du fonctionnement de tous les packages d’applications virtuelles incluant des brochures de script intégrées, qui disposent de fichiers de configurations dynamiques associés et de références et d’exécution des scripts de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="614bf-421">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="614bf-422">Supprimer les polices virtuelles superflues du package.</span><span class="sxs-lookup"><span data-stu-id="614bf-422">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-423">La plupart des applications examinées par l’équipe de produit App-V contenaient un petit nombre de polices, généralement moins de 20.</span><span class="sxs-lookup"><span data-stu-id="614bf-423">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-424">Les polices virtuelles influent sur les performances de la publication.</span><span class="sxs-lookup"><span data-stu-id="614bf-424">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="614bf-425">Les polices souhaitées devront être activées ou installées en mode natif.</span><span class="sxs-lookup"><span data-stu-id="614bf-425">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="614bf-426">Pour obtenir des instructions, voir installer ou désinstaller des polices.</span><span class="sxs-lookup"><span data-stu-id="614bf-426">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="614bf-427">Identifier les polices virtuelles qui existent dans le package</span><span class="sxs-lookup"><span data-stu-id="614bf-427">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="614bf-428">Effectuez une copie du package.</span><span class="sxs-lookup"><span data-stu-id="614bf-428">Make a copy of the package.</span></span>

-   <span data-ttu-id="614bf-429">Renommer le package \ _copy. AppV en Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="614bf-429">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="614bf-430">Ouvrez AppxManifest.xml et recherchez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="614bf-430">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="614bf-431">&lt;AppV: extension category = "AppV. polices"&gt;</span><span class="sxs-lookup"><span data-stu-id="614bf-431">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="614bf-432">&lt;AppV: polices&gt;</span><span class="sxs-lookup"><span data-stu-id="614bf-432">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="614bf-433">&lt;AppV: chemin de police = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /AppV: font&gt;</span><span class="sxs-lookup"><span data-stu-id="614bf-433">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="614bf-434">Remarque</span><span class="sxs-lookup"><span data-stu-id="614bf-434">Note</span></span>**  
    <span data-ttu-id="614bf-435">S’il existe des polices marquées comme **DelayLoad**, celles-ci n’ont aucun impact sur le premier lancement.</span><span class="sxs-lookup"><span data-stu-id="614bf-435">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="614bf-436">Exclusion de polices virtuelles du package</span><span class="sxs-lookup"><span data-stu-id="614bf-436">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="614bf-437">Utilisez le fichier de configuration dynamique qui correspond le mieux à la configuration de déploiement pour tous les utilisateurs sur un ordinateur, configuration utilisateur pour des utilisateurs ou des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="614bf-437">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="614bf-438">Désactiver les polices avec le déploiement ou la configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-438">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="614bf-439">Polices</span><span class="sxs-lookup"><span data-stu-id="614bf-439">Fonts</span></span>

--&gt;

<span data-ttu-id="614bf-440">&lt;Polices activées = "faux"/&gt;</span><span class="sxs-lookup"><span data-stu-id="614bf-440">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="614bf-441">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="614bf-441">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="614bf-442">Terminologie des recommandations en matière de performances de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="614bf-442">App-V 5.0 Performance Guidance Terminology</span></span>


<span data-ttu-id="614bf-443">Les termes suivants sont utilisés lors de la description des concepts et actions liés à l’optimisation des performances d’App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="614bf-443">The following terms are used when describing concepts and actions related to App-V 5.0 performance optimization.</span></span>

-   <span data-ttu-id="614bf-444">**Complexité** : désigne l’une ou plusieurs caractéristiques de package susceptibles d’avoir un impact sur les performances lors de la préconfiguration (**Add-AppvClientPackage**) ou de l’intégration (**publication-AppvClientPackage**).</span><span class="sxs-lookup"><span data-stu-id="614bf-444">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="614bf-445">Voici quelques exemples de caractéristiques: taille du manifeste, nombre de polices virtuelles, nombre de fichiers.</span><span class="sxs-lookup"><span data-stu-id="614bf-445">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="614bf-446">**Désintégration** : supprime les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-446">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="614bf-447">**Nouvelle intégration** : applique les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="614bf-447">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="614bf-448">**Non permanent, en regroupement** : crée un ordinateur exécutant un environnement virtuel chaque fois qu’il se connecte.</span><span class="sxs-lookup"><span data-stu-id="614bf-448">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="614bf-449">**Permanent et personnel** : ordinateur exécutant un environnement virtuel qui reste le même pour chaque connexion.</span><span class="sxs-lookup"><span data-stu-id="614bf-449">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="614bf-450">**État** -pour ce document, ce qui signifie que les intégrations des utilisateurs sont conservées entre les sessions et qu’une technologie de gestion de l’environnement utilisateur est utilisée en conjonction avec un hôte de session hôte ou VDI non persistant.</span><span class="sxs-lookup"><span data-stu-id="614bf-450">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="614bf-451">**Sans état** – représente un scénario dans lequel aucun état utilisateur n’est persistant entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="614bf-451">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="614bf-452">**Déclencheur** (déclencheur d’action natif).</span><span class="sxs-lookup"><span data-stu-id="614bf-452">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="614bf-453">UPM utilise ces types de déclencheurs pour lancer des opérations de surveillance ou de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="614bf-453">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="614bf-454">**Interface utilisateur** : dans le contexte de App-V 5,0, l’interface utilisateur, quantitativement, est la somme des parties suivantes:</span><span class="sxs-lookup"><span data-stu-id="614bf-454">**User Experience** - In the context of App-V 5.0, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="614bf-455">À partir du moment où les utilisateurs ouvrent une session pour pouvoir manipuler le bureau.</span><span class="sxs-lookup"><span data-stu-id="614bf-455">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="614bf-456">À partir du moment où le Bureau peut être utilisé pour une actualisation de publication (dans les termes de PowerShell, la synchronisation) lors de l’utilisation de l’infrastructure serveur complète App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="614bf-456">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.0 full server infrastructure.</span></span> <span data-ttu-id="614bf-457">Dans les instances autonomes, il s’agit du moment où les commandes PowerShell **Add-AppVClientPackage** et **Publish-AppVClientPackage** sont initialisées.</span><span class="sxs-lookup"><span data-stu-id="614bf-457">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="614bf-458">Du début à la fin de l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="614bf-458">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="614bf-459">Dans les instances autonomes, il s’agit de la première à la dernière application virtuelle publiée.</span><span class="sxs-lookup"><span data-stu-id="614bf-459">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="614bf-460">À partir du moment où l’application virtuelle est disponible pour le lancement à partir d’un raccourci.</span><span class="sxs-lookup"><span data-stu-id="614bf-460">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="614bf-461">Par ailleurs, il s’agit de l’emplacement d’enregistrement de l’Association de type de fichier et lancera une application virtuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="614bf-461">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="614bf-462">**Gestion des profils utilisateur** : l’approche contrôlée et structurée pour gérer les composants utilisateur associés à l’environnement.</span><span class="sxs-lookup"><span data-stu-id="614bf-462">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="614bf-463">Par exemple, profils utilisateur, gestion des préférences et de la stratégie, contrôle d’application et déploiement d’application.</span><span class="sxs-lookup"><span data-stu-id="614bf-463">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="614bf-464">Vous pouvez utiliser la création de scripts ou des solutions tierces pour configurer l’environnement selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="614bf-464">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="614bf-465">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="614bf-465">Related topics</span></span>


[<span data-ttu-id="614bf-466">Guide de l’administrateur de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="614bf-466">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)









