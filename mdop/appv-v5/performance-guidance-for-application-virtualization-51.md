---
title: Guide des performances pour Application Virtualization5.1
description: Guide des performances pour Application Virtualization5.1
author: dansimp
ms.assetid: 5f2643c7-5cf7-4a29-adb7-45bf9f5b0364
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3382a7958e12cc28b8101a6d5b7384a6975e6e82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805040"
---
# <span data-ttu-id="56893-103">Guide des performances pour Application Virtualization5.1</span><span class="sxs-lookup"><span data-stu-id="56893-103">Performance Guidance for Application Virtualization 5.1</span></span>


<span data-ttu-id="56893-104">Découvrez comment configurer App-V 5,1 pour obtenir des performances optimales, optimiser les packages d’application virtuelles et offrir une meilleure expérience utilisateur avec les services Bureau à distance et VDI.</span><span class="sxs-lookup"><span data-stu-id="56893-104">Learn how to configure App-V 5.1 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="56893-105">L’implémentation de plusieurs méthodes peut vous aider à améliorer l’utilisation de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="56893-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="56893-106">Toutefois, votre environnement ne prend pas en charge toutes les méthodes.</span><span class="sxs-lookup"><span data-stu-id="56893-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="56893-107">Nous vous conseillons de lire et de comprendre les informations suivantes avant de lire ce document.</span><span class="sxs-lookup"><span data-stu-id="56893-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="56893-108">Guide de l’administrateur de Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="56893-108">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="56893-109">Version de l’application et du client App-V 5 SP2</span><span class="sxs-lookup"><span data-stu-id="56893-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="56893-110">Guide de séquençage de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="56893-110">Microsoft Application Virtualization Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="56893-111">Remarque</span><span class="sxs-lookup"><span data-stu-id="56893-111">Note</span></span>**  
<span data-ttu-id="56893-112">Les termes utilisés dans ce document peuvent avoir une signification différente en fonction de la source et du contexte externes.</span><span class="sxs-lookup"><span data-stu-id="56893-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="56893-113">Pour plus d’informations sur les conditions d’utilisation de ce document, suivies d’un astérisque **\\** \*, voir la section [terminologie des recommandations](#bkmk-terms1) en matière de performances de la virtualisation d’applications de ce document.</span><span class="sxs-lookup"><span data-stu-id="56893-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="56893-114">Enfin, ce document vous fournit les informations nécessaires pour configurer l’ordinateur exécutant le client App-V 5,1 et l’environnement pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="56893-114">Finally, this document will provide you with the information to configure the computer running App-V 5.1 client and the environment for optimal performance.</span></span> <span data-ttu-id="56893-115">Optimisez vos packages d’applications virtuelles à des fins de performance à l’aide du Sequencer, et apprenez à utiliser les technologies de gestion de l’expérience utilisateur (UE-V) ou d’autres technologies de gestion de l’environnement utilisateur pour offrir une expérience utilisateur optimale avec App-V 5,1 dans les services Bureau à distance et les infrastructures de bureau virtuelles non persistantes.</span><span class="sxs-lookup"><span data-stu-id="56893-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.1 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="56893-116">Pour vous aider à déterminer quelles informations sont pertinentes pour votre environnement, vous devez consulter la liste rapide de chaque section et la liste de contrôle d’applicabilité.</span><span class="sxs-lookup"><span data-stu-id="56893-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-1-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="56893-117">App-V 5,1 dans des déploiements sans état persistant</span><span class="sxs-lookup"><span data-stu-id="56893-117">App-V 5.1 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="56893-118">Cette section fournit des informations sur une approche permettant de s’assurer que l’utilisateur a accès à toutes les applications virtuelles en quelques secondes après la connexion.</span><span class="sxs-lookup"><span data-stu-id="56893-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="56893-119">Pour cela, il suffit de traiter de manière unique l’actualisation de la publication de l’application-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="56893-119">This is achieved by uniquely addressing the often long-running App-V 5.1 publishing refresh.</span></span> <span data-ttu-id="56893-120">Comme vous le découvrirez le niveau de base de l’approche, l’actualisation de publication la plus rapide est d’une qui ne doit pas réellement faire quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="56893-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="56893-121">Un certain nombre de conditions doivent être respectées et suivre les étapes pour offrir une expérience utilisateur optimale.</span><span class="sxs-lookup"><span data-stu-id="56893-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="56893-122">Pour plus d’informations, utilisez les informations fournies dans la section suivante:</span><span class="sxs-lookup"><span data-stu-id="56893-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="56893-123">[Scénarios d’utilisation](#bkmk-us) : lorsque vous passez en revue les deux scénarios, gardez à l’esprit qu’il s’agit de l’approche extrême.</span><span class="sxs-lookup"><span data-stu-id="56893-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="56893-124">En fonction de vos besoins en matière d’utilisation, vous pouvez choisir d’appliquer ces étapes à un sous-ensemble d’utilisateurs et/ou de packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="56893-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="56893-125">Optimisée pour les performances: pour offrir une expérience optimale, vous pouvez vous attendre que l’image de base inclue une partie du package d’application virtuelle App-V.</span><span class="sxs-lookup"><span data-stu-id="56893-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="56893-126">Cette configuration est abordée.</span><span class="sxs-lookup"><span data-stu-id="56893-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="56893-127">Optimisé pour le stockage: Si vous vous souciez de l’impact sur le stockage, suivez ce scénario pour mieux répondre à ces inquiétudes.</span><span class="sxs-lookup"><span data-stu-id="56893-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="56893-128">Préparation de votre environnement</span><span class="sxs-lookup"><span data-stu-id="56893-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="56893-129">Étapes à suivre pour préparer l’image de base, que ce soit dans un environnement VDI ou hôte non persistant, seules quelques étapes doivent être effectuées dans l’image de base pour activer cette approche.</span><span class="sxs-lookup"><span data-stu-id="56893-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="56893-130">Utiliser UE-V 2,1 comme solution de gestion des profils utilisateur pour l’approche App-V: la pierre angulaire de cette approche est la capacité d’une solution UEM de conserver le contenu de quelques emplacements de Registre et de fichiers.</span><span class="sxs-lookup"><span data-stu-id="56893-130">Use UE-V 2.1 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="56893-131">Ces lieux constituent les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="56893-132">Veillez à consulter la configuration requise pour la solution UPM.</span><span class="sxs-lookup"><span data-stu-id="56893-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="56893-133">Utilisation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="56893-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="56893-134">Procédure pas à pas: il s’agit d’une procédure pas à pas illustrant les opérations App-V et UE-V ainsi que les attentes des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="56893-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="56893-135">Résultat: cette opération décrit les résultats attendus.</span><span class="sxs-lookup"><span data-stu-id="56893-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="56893-136">Impact sur le cycle de vie des packages</span><span class="sxs-lookup"><span data-stu-id="56893-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="56893-137">Amélioration de l’interface VDI via l’optimisation et l’optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="56893-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="56893-138">Liste de vérification d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="56893-138">Applicability Checklist</span></span>

<span data-ttu-id="56893-139">Environnement de déploiement</span><span class="sxs-lookup"><span data-stu-id="56893-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="56893-140">VDI ou hôte non persistant.</span><span class="sxs-lookup"><span data-stu-id="56893-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="56893-141">La virtualisation de l’interface utilisateur (UE-V), les autres solutions UPM ou les disques de profil utilisateur (UPD).</span><span class="sxs-lookup"><span data-stu-id="56893-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="56893-142">Configuration prévue</span><span class="sxs-lookup"><span data-stu-id="56893-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="56893-143">Virtualisation de l’utilisation des utilisateurs (UE-V) avec le modèle d’état utilisateur App-V activé ou le logiciel de gestion des profils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="56893-144">Le logiciel de UPM sans UE-V doit être capable de déclencher le déclenchement de la connexion ou du démarrage de processus/application.</span><span class="sxs-lookup"><span data-stu-id="56893-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="56893-145">Le magasin de contenus partagés App-V (SCS) est configuré ou peut être configuré.</span><span class="sxs-lookup"><span data-stu-id="56893-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="56893-146">Administration informatique</span><span class="sxs-lookup"><span data-stu-id="56893-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="56893-147">Il est possible que l’administrateur ait besoin de mettre à jour l’image de base de l’ordinateur virtuel pour garantir des performances optimales ou s’il doit gérer plusieurs images pour différents groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="56893-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="56893-148">Scénario d’utilisation</span><span class="sxs-lookup"><span data-stu-id="56893-148">Usage Scenario</span></span>

<span data-ttu-id="56893-149">Lorsque vous passez en revue les deux scénarios, gardez à l’esprit que ces deux approches sont extrêmes.</span><span class="sxs-lookup"><span data-stu-id="56893-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="56893-150">En fonction de vos besoins en matière d’utilisation, vous pouvez choisir d’appliquer ces étapes à un sous-ensemble d’utilisateurs, des packages d’applications virtuelles ou les deux.</span><span class="sxs-lookup"><span data-stu-id="56893-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56893-151">Optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="56893-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="56893-152">Optimisé pour le stockage</span><span class="sxs-lookup"><span data-stu-id="56893-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56893-153">Pour fournir une utilisation optimale de l’utilisateur, cette approche exploite les fonctionnalités d’une solution UPM et nécessite une préparation supplémentaire de l’image et peut occasionner une surcharge supplémentaire de gestion des images.</span><span class="sxs-lookup"><span data-stu-id="56893-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="56893-154">Ce qui suit décrit de nombreuses améliorations des performances dans les déploiements sans état persistants.</span><span class="sxs-lookup"><span data-stu-id="56893-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="56893-155">Pour plus d’informations, reportez-vous <strong> aux étapes de séquençage pour optimiser les packages pour les performances de publication </strong> et la référence au <strong> Guide de séquençage App-V </strong> dans la <strong> section Voir aussi de ce document </strong> .</span><span class="sxs-lookup"><span data-stu-id="56893-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-156">Les attentes générales du scénario précédent continuent de s’appliquer ici.</span><span class="sxs-lookup"><span data-stu-id="56893-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="56893-157">Néanmoins, gardez à l’esprit que les images VM sont généralement stockées dans des tableaux très coûteux; une légère modification a été apportée à l’approche.</span><span class="sxs-lookup"><span data-stu-id="56893-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="56893-158">Ne configurez pas les packages d’application virtuelle ciblés par l’utilisateur dans l’image de base.</span><span class="sxs-lookup"><span data-stu-id="56893-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="56893-159">L’impact de cette modification est décrit dans la section démonstration de l’utilisation de l’utilisateur de ce document.</span><span class="sxs-lookup"><span data-stu-id="56893-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="56893-160">Préparation de votre environnement</span><span class="sxs-lookup"><span data-stu-id="56893-160">Preparing your Environment</span></span>

<span data-ttu-id="56893-161">Le tableau suivant répertorie les étapes nécessaires pour préparer l’image de base et l’UE-V ou une autre solution UPM pour l’approche.</span><span class="sxs-lookup"><span data-stu-id="56893-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="56893-162">Préparer l’image de base</span><span class="sxs-lookup"><span data-stu-id="56893-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56893-163">Optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="56893-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="56893-164">Optimisé pour le stockage</span><span class="sxs-lookup"><span data-stu-id="56893-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="56893-165">Installez la version cliente App-V 5,1 du client.</span><span class="sxs-lookup"><span data-stu-id="56893-165">Install the App-V 5.1 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="56893-166">Pour installer UE-V et télécharger le modèle de paramètres App-V à partir de la Galerie de modèles UE-V, voir les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="56893-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="56893-167">Configurer pour le mode de magasin de contenus partagés (SCS).</span><span class="sxs-lookup"><span data-stu-id="56893-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="56893-168">Pour plus d’informations, reportez-vous <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> à l’installation du client App-V 5,1 pour le mode magasin de contenu partagé </a> .</span><span class="sxs-lookup"><span data-stu-id="56893-168">For more information see <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)">How to Install the App-V 5.1 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="56893-169">Configurez les intégrations utilisateur dans Registre de connexion DWORD.</span><span class="sxs-lookup"><span data-stu-id="56893-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="56893-170">Préconfigurer tous les packages ciblés par l’utilisateur et le niveau global (par exemple, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="56893-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="56893-171">Préconfigurer tous les groupes de connexions ciblés par l’utilisateur et le niveau global, par exemple, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="56893-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="56893-172">Publiez préalablement tous les packages destinés au global.</span><span class="sxs-lookup"><span data-stu-id="56893-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="56893-173">Vous pouvez également</span><span class="sxs-lookup"><span data-stu-id="56893-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-174">Effectuer une publication/actualisation globale.</span><span class="sxs-lookup"><span data-stu-id="56893-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="56893-175">Effectuer une publication/actualisation utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="56893-176">Annulez la publication de tous les packages ciblés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="56893-177">Supprimez les entrées de système de fichiers virtuelles utilisateur (VFS) suivantes.</span><span class="sxs-lookup"><span data-stu-id="56893-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="56893-178">Installez la version cliente App-V 5,1 du client.</span><span class="sxs-lookup"><span data-stu-id="56893-178">Install the App-V 5.1 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="56893-179">Pour installer UE-V et télécharger le modèle de paramètres App-V à partir de la Galerie de modèles UE-V, voir les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="56893-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="56893-180">Configurer pour le mode de magasin de contenus partagés (SCS).</span><span class="sxs-lookup"><span data-stu-id="56893-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="56893-181">Pour plus d’informations, reportez-vous <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> à l’installation du client App-V 5,1 pour le mode magasin de contenu partagé </a> .</span><span class="sxs-lookup"><span data-stu-id="56893-181">For more information see <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)">How to Install the App-V 5.1 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="56893-182">Configurez les intégrations utilisateur dans Registre de connexion DWORD.</span><span class="sxs-lookup"><span data-stu-id="56893-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="56893-183">Préconfigurer tous les packages ciblés globalement par exemple, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="56893-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="56893-184">Configurez tous les groupes de connexions cibles globales, par exemple, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="56893-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="56893-185">Publiez préalablement tous les packages destinés au global.</span><span class="sxs-lookup"><span data-stu-id="56893-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="56893-186">**Configurations** -pour les configurations de client d’application V critiques et pour un peu plus de contexte et de procédure, consultez les informations suivantes:</span><span class="sxs-lookup"><span data-stu-id="56893-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56893-187">Paramètre de configuration</span><span class="sxs-lookup"><span data-stu-id="56893-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="56893-188">Qu’est-ce que c’est?</span><span class="sxs-lookup"><span data-stu-id="56893-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="56893-189">Comment dois-je l’utiliser?</span><span class="sxs-lookup"><span data-stu-id="56893-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56893-190">Mode de magasin de contenus partagés (SCS)</span><span class="sxs-lookup"><span data-stu-id="56893-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-191">Configurable dans PowerShell à l’aide de <strong> Set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> ou</span><span class="sxs-lookup"><span data-stu-id="56893-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="56893-192">Lors de l’installation du client App-V.</span><span class="sxs-lookup"><span data-stu-id="56893-192">During installation of the App-V client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="56893-193">Lors de l’exécution du magasin de contenu partagé, seules les données de publication sont conservées sur le disque dur; les autres ressources d’application virtuelles sont conservées en mémoire (RAM).</span><span class="sxs-lookup"><span data-stu-id="56893-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="56893-194">Cela permet de conserver le stockage local et de réduire les e/s de disque par seconde (IOPS).</span><span class="sxs-lookup"><span data-stu-id="56893-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-195">Cette option est recommandée lorsque les connexions à faible latence sont disponibles entre le point de terminaison du client App-V et le serveur de contenu SCS.</span><span class="sxs-lookup"><span data-stu-id="56893-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56893-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="56893-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-197">Configurer dans le Registre sous <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> </strong>  \  <strong> intégration du </strong>  \  <strong> client Microsoft AppV </strong>  \  <strong> </strong>  \  <strong> </strong> du logiciel.</span><span class="sxs-lookup"><span data-stu-id="56893-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="56893-198">Créez la valeur DWORD <strong> PreserveUserIntegrationsOnLogin </strong> avec la valeur <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="56893-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="56893-199">Redémarrez le service client App-V ou redémarrez l’ordinateur exécutant le client App-V.</span><span class="sxs-lookup"><span data-stu-id="56893-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="56893-200">Si vous n’avez pas encore préconfiguré ( <strong> Add-AppvClientPackage </strong> ) d’un package spécifique et que ce paramètre n’est pas configuré, le client App-V va de nouveau intégrer \* les intégrations utilisateur persistantes, puis réintégrer \*.</span><span class="sxs-lookup"><span data-stu-id="56893-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="56893-201">Pour tous les packages qui remplissent les conditions ci-dessus, il est plus efficace de procéder au travail lors de la publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="56893-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-202">Si vous envisagez de préconfigurer tous les packages d’utilisateurs disponibles dans l’image de base, utilisez ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="56893-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56893-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="56893-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-204">Configurez le registre dans le Registre sous HKEY_LOCAL_MACHINE publications puissantes du <strong> </strong> &lt; &gt; </strong>  \  <strong> </strong>  \  <strong> client Microsoft AppV </strong> &lt; &gt; </strong>  \  <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="56893-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="56893-205">Créez la valeur DWORD <strong> MaxConcurrentPublishingrefresh </strong> en utilisant le nombre maximal de rafraîchissements simultanés de la publication.</span><span class="sxs-lookup"><span data-stu-id="56893-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="56893-206">Il n’est pas nécessaire de relancer le service client et l’ordinateur App-V.</span><span class="sxs-lookup"><span data-stu-id="56893-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="56893-207">Ce paramètre détermine le nombre d’utilisateurs qui peuvent effectuer une actualisation ou une synchronisation de publication en même temps.</span><span class="sxs-lookup"><span data-stu-id="56893-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="56893-208">Le paramètre par défaut est sans limite.</span><span class="sxs-lookup"><span data-stu-id="56893-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-209">Limiter le nombre de rafraîchissements de publication simultanées évite une utilisation excessive de l’UC qui peut affecter les performances de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="56893-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="56893-210">Cette limite est recommandée dans un environnement RDS, où plusieurs utilisateurs peuvent se connecter au même ordinateur en même temps et effectuer une synchronisation d’actualisation de publication.</span><span class="sxs-lookup"><span data-stu-id="56893-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="56893-211">Si le seuil d’actualisation de publication simultanée est atteint, le temps requis pour publier de nouvelles applications et les mettre à la disposition des utilisateurs finaux après leur connexion peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="56893-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="56893-212">Configurer une solution UE-V pour l’approche App-v</span><span class="sxs-lookup"><span data-stu-id="56893-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="56893-213">Nous vous recommandons d’utiliser la virtualisation de l’utilisation de Microsoft User (UE-V) pour capturer et centraliser les paramètres d’application et les paramètres du système d’exploitation Windows pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="56893-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="56893-214">Ces paramètres sont ensuite appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="56893-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="56893-215">UE-V est optimisée pour les scénarios RDS et VDI.</span><span class="sxs-lookup"><span data-stu-id="56893-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="56893-216">Pour plus d’informations, reportez-vous [à la rubrique mise en route de l’interface utilisateur-virtualisation 2,0](https://technet.microsoft.com/library/dn458926.aspx)</span><span class="sxs-lookup"><span data-stu-id="56893-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458926.aspx)</span></span>

<span data-ttu-id="56893-217">Par essence, il est nécessaire d’installer le client UE-V et de télécharger le modèle de paramètres App-v Microsoft créé à partir de la [Galerie de modèles Microsoft User Interface (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span><span class="sxs-lookup"><span data-stu-id="56893-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="56893-218">Enregistrez le modèle.</span><span class="sxs-lookup"><span data-stu-id="56893-218">Register the template.</span></span> <span data-ttu-id="56893-219">Pour plus d’informations sur les modèles UE-V, voir [la ressource spécifique d’UE-v pour l’acquisition et l’inscription du modèle](https://technet.microsoft.com/library/dn458926.aspx).</span><span class="sxs-lookup"><span data-stu-id="56893-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458926.aspx).</span></span>

**<span data-ttu-id="56893-220">Remarque</span><span class="sxs-lookup"><span data-stu-id="56893-220">Note</span></span>**  
<span data-ttu-id="56893-221">Sans exécuter une étape de configuration supplémentaire, la virtualisation de l’environnement utilisateur Microsoft (UE-V) ne sera pas en mesure de synchroniser les raccourcis du menu Démarrer (fichiers. lnk) sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="56893-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="56893-222">Le type de fichier. lnk est exclu par défaut.</span><span class="sxs-lookup"><span data-stu-id="56893-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="56893-223">UE-V ne prend en charge que la suppression du type de fichier. lnk de la liste d’exclusions dans les scénarios RDS et VDI, où l’appareil de chaque utilisateur dispose du même ensemble d’applications installées sur le même emplacement et chaque fichier. lnk est valide pour tous les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="56893-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="56893-224">Par exemple, UE-V ne prend pas en charge les 2 scénarios suivants, car le résultat net sera valide sur un seul, mais pas sur tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="56893-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="56893-225">Si un utilisateur dispose d’une application installée sur un appareil avec fichiers. lnk activés et de la même application native installée sur un autre appareil à une autre racine d’installation avec les fichiers. lnk activés.</span><span class="sxs-lookup"><span data-stu-id="56893-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="56893-226">Si un utilisateur a installé une application sur un appareil, mais pas un autre avec des fichiers. lnk activés.</span><span class="sxs-lookup"><span data-stu-id="56893-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="56893-227">Important</span><span class="sxs-lookup"><span data-stu-id="56893-227">Important</span></span>**  
<span data-ttu-id="56893-228">Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="56893-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="56893-229">Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows.</span><span class="sxs-lookup"><span data-stu-id="56893-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="56893-230">Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre.</span><span class="sxs-lookup"><span data-stu-id="56893-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="56893-231">Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus.</span><span class="sxs-lookup"><span data-stu-id="56893-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="56893-232">Changez de Registre à vos propres risques.</span><span class="sxs-lookup"><span data-stu-id="56893-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="56893-233">À l’aide de l’éditeur du Registre Microsoft (regedit.exe), accédez à la section **HKEY \ _LOCAL \ _MACHINE**  \\  **logiciel**  \\  **Microsoft**  \\  **UEV**  \\  **agent**  \\  **configuration**  \\  **ExcludedFileTypes** et supprimez le fichier **. lnk** des types de fichiers exclus.</span><span class="sxs-lookup"><span data-stu-id="56893-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="56893-234">Configurer une solution de gestion des profils utilisateur pour l’application-V</span><span class="sxs-lookup"><span data-stu-id="56893-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="56893-235">L’attente dans un environnement avec état est qu’une solution UPM est implémentée et peut prendre en charge la persistance des données utilisateur entre des sessions et entre des connexions.</span><span class="sxs-lookup"><span data-stu-id="56893-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="56893-236">La configuration requise pour la solution UPM est la suivante:</span><span class="sxs-lookup"><span data-stu-id="56893-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="56893-237">Pour garantir une expérience de connexion optimisée (par exemple, l’approche App-V 5,1 pour l’utilisateur), la solution doit être capable de:</span><span class="sxs-lookup"><span data-stu-id="56893-237">To enable an optimized login experience, for example the App-V 5.1 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="56893-238">La conservation des intégrations utilisateur dans le cadre du profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="56893-239">Le déclenchement d’une synchronisation de profil utilisateur à l’ouverture de session (ou de début de l’application), qui peut garantir l’application de toutes les intégrations utilisateur avant le début de la publication/actualisation; ou</span><span class="sxs-lookup"><span data-stu-id="56893-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="56893-240">Attachement et détachement d’un disque de profil utilisateur ou d’une technologie similaire contenant les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

    **<span data-ttu-id="56893-241">Remarque</span><span class="sxs-lookup"><span data-stu-id="56893-241">Note</span></span>**  
    <span data-ttu-id="56893-242">App-V est pris en charge dans le cadre de l’utilisation de UPD uniquement lorsque le profil complet est stocké sur le disque de profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-242">App-V is supported when using UPD only when the entire profile is stored on the user profile disk.</span></span>

    <span data-ttu-id="56893-243">Les packages App-V ne sont pas pris en charge lors de l’utilisation de UPD avec des dossiers sélectionnés stockés sur le disque de profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-243">App-V packages are not supported when using UPD with selected folders stored in the user profile disk.</span></span> <span data-ttu-id="56893-244">Le pilote de copie sur écriture ne gère pas les dossiers sélectionnés UPD.</span><span class="sxs-lookup"><span data-stu-id="56893-244">The Copy on Write driver does not handle UPD selected folders.</span></span>



-   <span data-ttu-id="56893-245">Capture des modifications apportées aux emplacements, qui constituent les intégrations utilisateur, avant la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="56893-245">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="56893-246">Avec App-V 5,1 lorsque vous ajoutez un serveur de publication (**Add-AppvPublishingServer**), vous pouvez configurer la synchronisation, par exemple pour l’actualisation lors de la connexion et/ou après un intervalle d’actualisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="56893-246">With App-V 5.1 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="56893-247">Dans les deux cas, une tâche planifiée est créée.</span><span class="sxs-lookup"><span data-stu-id="56893-247">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="56893-248">Dans les versions précédentes de App-V 5,1, les deux tâches planifiées ont été configurées à l’aide d’un code VBScript qui initierait l’actualisation globale et de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-248">In previous versions of App-V 5.1, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="56893-249">Le correctif logiciel 4 pour l’application virtualisation de l’application 5,0 SP2 est lancé par **SyncAppvPublishingServer.exe**.</span><span class="sxs-lookup"><span data-stu-id="56893-249">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on was initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="56893-250">Cette modification a été apportée de manière à fournir des solutions UPM comme processus de déclenchement.</span><span class="sxs-lookup"><span data-stu-id="56893-250">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="56893-251">Ce processus retarde la publication/Refresh pour permettre à la solution UPM d’appliquer les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-251">This process delays the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="56893-252">Elle se fermera une fois que la publication/actualisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="56893-252">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="56893-253">Intégrations utilisateur</span><span class="sxs-lookup"><span data-stu-id="56893-253">User Integrations</span></span>**

<span data-ttu-id="56893-254">Registry-HKEY \ _CURRENT \ _USER</span><span class="sxs-lookup"><span data-stu-id="56893-254">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="56893-255">Path-Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="56893-255">Path - Software\\Classes</span></span>

    <span data-ttu-id="56893-256">Exclude: Local Settings, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="56893-256">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="56893-257">Path-Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="56893-257">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="56893-258">Chemins d’accès-Software\\Microsoft\\Windows\\CurrentVersion\\App</span><span class="sxs-lookup"><span data-stu-id="56893-258">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="56893-259">Emplacement des fichiers</span><span class="sxs-lookup"><span data-stu-id="56893-259">File Locations</span></span>**

-   <span data-ttu-id="56893-260">Root – «variable d’environnement» APPDATA</span><span class="sxs-lookup"><span data-stu-id="56893-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="56893-261">Path – Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="56893-261">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="56893-262">Root – «variable d’environnement» APPDATA</span><span class="sxs-lookup"><span data-stu-id="56893-262">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="56893-263">Path – Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="56893-263">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="56893-264">Root – «variable d’environnement» APPDATA</span><span class="sxs-lookup"><span data-stu-id="56893-264">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="56893-265">Path-Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="56893-265">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="56893-266">(Pour conserver tous les raccourcis bureau, virtuels et non virtuels)</span><span class="sxs-lookup"><span data-stu-id="56893-266">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="56893-267">Root-«KnownFolder» {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ \*. lnk</span><span class="sxs-lookup"><span data-stu-id="56893-267">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="56893-268">Virtualisation de l’utilisation de Microsoft User (UE-V)</span><span class="sxs-lookup"><span data-stu-id="56893-268">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="56893-269">Par ailleurs, nous vous conseillons d’utiliser Microsoft User Interface Virtualization (UE-V) pour capturer et centraliser les paramètres d’application et les paramètres du système d’exploitation Windows pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="56893-269">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="56893-270">Ces paramètres sont ensuite appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="56893-270">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="56893-271">Pour plus d’informations, reportez-vous à la rubrique [mise en route de l’utilisation de l’interface utilisateur 1,0](https://technet.microsoft.com/library/jj680015.aspx) et [partage de modèles d’emplacement des paramètres avec la Galerie de modèles UE-V](https://technet.microsoft.com/library/jj679972.aspx).</span><span class="sxs-lookup"><span data-stu-id="56893-271">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="56893-272">Utilisation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="56893-272">User Experience Walk-through</span></span>

<span data-ttu-id="56893-273">Vous trouverez ci-dessous une procédure pas à pas illustrant les opérations d’application-V et de UPM, ainsi que les attentes des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="56893-273">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56893-274">Optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="56893-274">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="56893-275">Optimisé pour le stockage</span><span class="sxs-lookup"><span data-stu-id="56893-275">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56893-276">Après l’implémentation de cette approche dans l’environnement VDI/hôte de connexion à la première connexion,</span><span class="sxs-lookup"><span data-stu-id="56893-276">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-277">Activité Un utilisateur-publication/actualisation est lancé.</span><span class="sxs-lookup"><span data-stu-id="56893-277">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="56893-278">Attente S’il s’agit de la première fois qu’un utilisateur a publié des applications virtuelles (par exemple, non persistant), la durée de publication et de rafraîchissement est normale.</span><span class="sxs-lookup"><span data-stu-id="56893-278">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="56893-279">Activité Après la publication et l’actualisation, la solution UPM capture les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-279">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="56893-280">Attente En fonction de la configuration de la solution UPM, cela peut se produire dans le cadre du processus de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="56893-280">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="56893-281">Cette opération entraîne la conservation de l’état utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-281">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="56893-282">Sur les connexions suivantes:</span><span class="sxs-lookup"><span data-stu-id="56893-282">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-283">Activité La solution UPM applique les intégrations utilisateur au système avant la publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="56893-283">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="56893-284">Attente Des raccourcis apparaissent sur votre ordinateur de bureau, ou dans le menu Démarrer, qui fonctionne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="56893-284">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="56893-285">Lorsque la publication ou l’actualisation est terminée (par exemple, le changement de package), certains risquent de ne pas être déplacés.</span><span class="sxs-lookup"><span data-stu-id="56893-285">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="56893-286">Activité Le processus de publication/actualisation traitera les opérations d’annulation de publication et de publication des modifications apportées aux habilitations du package utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-286">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="56893-287">Attente S’il n’y a aucune modification d’habilitation, publishing1 se termine en quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="56893-287">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="56893-288">Dans le cas contraire, le nombre et la complexité de la publication et de la mise à jour des applications virtuelles seront augmentés.</span><span class="sxs-lookup"><span data-stu-id="56893-288">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="56893-289">Activité La solution UPM répartira les intégrations des utilisateurs lors de la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="56893-289">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="56893-290">Attente Comme précédent.</span><span class="sxs-lookup"><span data-stu-id="56893-290">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="56893-291">¹ l’opération de publication ( <strong> publication-AppVClientPackage </strong> ) ajoute des entrées au catalogue de l’utilisateur, des cartes de habilitation pour l’utilisateur, identifie le magasin local et se termine en effectuant les étapes d’intégration.</span><span class="sxs-lookup"><span data-stu-id="56893-291">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-292">Après l’implémentation de cette approche dans l’environnement VDI/hôte de connexion à la première connexion,</span><span class="sxs-lookup"><span data-stu-id="56893-292">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-293">Activité Un utilisateur-publication/actualisation est lancé.</span><span class="sxs-lookup"><span data-stu-id="56893-293">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="56893-294">Attente</span><span class="sxs-lookup"><span data-stu-id="56893-294">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-295">S’il s’agit de la première fois qu’un utilisateur a publié des applications virtuelles (par exemple, non persistant), cette méthode prend la durée habituelle d’une publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="56893-295">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="56893-296">Les connexions préalables et suivantes seront affectées en préconfigurant les packages (Ajouter/actualiser).</span><span class="sxs-lookup"><span data-stu-id="56893-296">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="56893-297">Activité Après la publication et l’actualisation, la solution UPM capture les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-297">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="56893-298">Attente En fonction de la configuration de la solution UPM, cela peut se produire dans le cadre du processus de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="56893-298">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="56893-299">Cela entraînera la même surcharge ou une surcharge similaire à la conservation de l’état utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-299">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="56893-300">Sur les connexions suivantes:</span><span class="sxs-lookup"><span data-stu-id="56893-300">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-301">Activité La solution UPM applique les intégrations utilisateur au système avant la publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="56893-301">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="56893-302">Activité L’ajout/actualisation doit préconfigurer toutes les applications ciblées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-302">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="56893-303">Attente</span><span class="sxs-lookup"><span data-stu-id="56893-303">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-304">Cela peut ralentir considérablement la disponibilité des applications (selon une période de 10 secondes).</span><span class="sxs-lookup"><span data-stu-id="56893-304">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="56893-305">Cela augmente l’heure d’actualisation de publication par rapport au nombre et à la complexité \* des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="56893-305">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="56893-306">Activité La publication et l’actualisation traitent les opérations d’annulation de la publication et de publication des modifications apportées aux habilitations du package d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-306">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
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
<th align="left"><span data-ttu-id="56893-307">About</span><span class="sxs-lookup"><span data-stu-id="56893-307">Outcome</span></span></th>
<th align="left"><span data-ttu-id="56893-308">About</span><span class="sxs-lookup"><span data-stu-id="56893-308">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="56893-309">Dans la mesure où les intégrations utilisateur sont entièrement préservées, il n’y a pas de tâche, par exemple, l’intégration de l’opération de publication/actualisation.</span><span class="sxs-lookup"><span data-stu-id="56893-309">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="56893-310">Toutes les applications virtuelles seront disponibles en quelques secondes de connexion.</span><span class="sxs-lookup"><span data-stu-id="56893-310">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="56893-311">La publication/actualisation traite les modifications apportées aux utilisateurs ayant des applications virtuelles qui ont une incidence sur l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-311">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="56893-312">Dans la mesure où l’ajout/actualisation doit reconfigurer toutes les applications virtuelles sur la machine virtuelle, le délai d’actualisation de publication sur chaque connexion sera prolongé.</span><span class="sxs-lookup"><span data-stu-id="56893-312">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="56893-313">Impact sur le cycle de vie d’un package</span><span class="sxs-lookup"><span data-stu-id="56893-313">Impact to Package Life Cycle</span></span>

<span data-ttu-id="56893-314">La mise à niveau d’un package est un aspect essentiel du cycle de vie du package.</span><span class="sxs-lookup"><span data-stu-id="56893-314">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="56893-315">Pour garantir que les utilisateurs ont accès aux packages d’applications virtuelles mis à niveau appropriés (publiés) ou mis à niveau (non publié), il est recommandé de mettre à jour l’image de base pour refléter ces modifications.</span><span class="sxs-lookup"><span data-stu-id="56893-315">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="56893-316">Pour mieux comprendre pourquoi examinez la section suivante:</span><span class="sxs-lookup"><span data-stu-id="56893-316">To understand why review the following section:</span></span>

<span data-ttu-id="56893-317">App-V 5,0 SP2 a instauré le concept d’États en attente.</span><span class="sxs-lookup"><span data-stu-id="56893-317">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="56893-318">Par le passé,</span><span class="sxs-lookup"><span data-stu-id="56893-318">In the past,</span></span>

-   <span data-ttu-id="56893-319">Si un administrateur a changé d’habilitation ou a créé une nouvelle version d’un package (mise à niveau) et, au cours d’une publication/actualisation, le package était en cours d’utilisation, l’opération d’annulation de publication</span><span class="sxs-lookup"><span data-stu-id="56893-319">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="56893-320">À présent, si un package est en cours d’utilisation, l’opération est en attente.</span><span class="sxs-lookup"><span data-stu-id="56893-320">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="56893-321">Les opérations d’annulation de publication et de publication en attente seront traitées lors du redémarrage du service ou si une autre commande publier ou annuler la publication est émise.</span><span class="sxs-lookup"><span data-stu-id="56893-321">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="56893-322">Dans ce dernier cas, si l’application virtuelle est en cours d’utilisation, l’application virtuelle reste dans un état d’attente.</span><span class="sxs-lookup"><span data-stu-id="56893-322">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="56893-323">Pour les packages publiés globalement, un redémarrage (ou un redémarrage du service) est souvent nécessaire.</span><span class="sxs-lookup"><span data-stu-id="56893-323">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="56893-324">Dans un environnement non persistant, il est peu probable que les opérations en attente soient traitées.</span><span class="sxs-lookup"><span data-stu-id="56893-324">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="56893-325">Les opérations en attente, par exemple les tâches sont capturées sous **HKEY \ _CURRENT \ _USER**  \\  **logiciel**  \\  **Microsoft**  \\  **AppV**  \\  **client**  \\  **PendingTasks**.</span><span class="sxs-lookup"><span data-stu-id="56893-325">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="56893-326">Même si cet emplacement est persistant par la solution UPM, si elle n’est pas appliquée à l’environnement avant de se connecter, ce dernier ne sera pas traité.</span><span class="sxs-lookup"><span data-stu-id="56893-326">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="56893-327">Amélioration de l’interface VDI par le biais de l’optimisation des performances</span><span class="sxs-lookup"><span data-stu-id="56893-327">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="56893-328">La section suivante contient des listes contenant des informations sur les documents et les téléchargements Microsoft qui pourraient s’avérer utiles lors de l’optimisation de votre environnement en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="56893-328">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="56893-329">Blog et script .NET NGEN (vivement recommandé)</span><span class="sxs-lookup"><span data-stu-id="56893-329">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="56893-330">À propos de la technologie NGEN</span><span class="sxs-lookup"><span data-stu-id="56893-330">About NGEN technology</span></span>

-   [<span data-ttu-id="56893-331">Comment accélérer l’optimisation de NGEN</span><span class="sxs-lookup"><span data-stu-id="56893-331">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="56893-332">Script</span><span class="sxs-lookup"><span data-stu-id="56893-332">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="56893-333">Rôles serveur et serveur Windows</span><span class="sxs-lookup"><span data-stu-id="56893-333">Windows Server and Server Roles</span></span>**

<span data-ttu-id="56893-334">Recommandations en matière d’optimisation des performances du serveur pour</span><span class="sxs-lookup"><span data-stu-id="56893-334">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="56893-335">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="56893-335">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="56893-336">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56893-336">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="56893-337">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="56893-337">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="56893-338">Rôles de serveur</span><span class="sxs-lookup"><span data-stu-id="56893-338">Server Roles</span></span>**

-   [<span data-ttu-id="56893-339">Hôte de virtualisation du Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="56893-339">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="56893-340">Hôte de session Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="56893-340">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="56893-341">Pertinence IIS: gestion d’App-V, publication, création de rapports Web services</span><span class="sxs-lookup"><span data-stu-id="56893-341">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="56893-342">Pertinence du serveur de fichiers (SMB): s’il est utilisé pour le stockage et la remise des contenus App-V dans le mode SCS</span><span class="sxs-lookup"><span data-stu-id="56893-342">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="56893-343">Recommandations en matière d’optimisation des performances de client Windows (système d’exploitation invité)</span><span class="sxs-lookup"><span data-stu-id="56893-343">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="56893-344">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="56893-344">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="56893-345">Script d’optimisation: (fourni par le support Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56893-345">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="56893-346">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="56893-346">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="56893-347">Script d’optimisation: (fourni par le support Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56893-347">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="56893-348">Étapes de séquençage pour optimiser les packages de performance de publication</span><span class="sxs-lookup"><span data-stu-id="56893-348">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="56893-349">Plusieurs fonctionnalités d’application V permettent de créer de nouveaux scénarios ou d’activer de nouveaux scénarios de déploiement de clients.</span><span class="sxs-lookup"><span data-stu-id="56893-349">Several App-V features facilitate new scenarios or enable new customer deployment scenarios.</span></span> <span data-ttu-id="56893-350">Les fonctionnalités suivantes peuvent avoir un impact sur les performances des opérations de publication et de lancement.</span><span class="sxs-lookup"><span data-stu-id="56893-350">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56893-351">Étape</span><span class="sxs-lookup"><span data-stu-id="56893-351">Step</span></span></th>
<th align="left"><span data-ttu-id="56893-352">Facteur</span><span class="sxs-lookup"><span data-stu-id="56893-352">Consideration</span></span></th>
<th align="left"><span data-ttu-id="56893-353">Avantages</span><span class="sxs-lookup"><span data-stu-id="56893-353">Benefits</span></span></th>
<th align="left"><span data-ttu-id="56893-354">Compromis</span><span class="sxs-lookup"><span data-stu-id="56893-354">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56893-355">Aucun bloc de fonctionnalité 1 (FB1, également connu sous le nom de FB-principal)</span><span class="sxs-lookup"><span data-stu-id="56893-355">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-356">Non FB1 indique que l’application sera lancée immédiatement et qu’elle nécessite une erreur de type fichier (l’application nécessite un fichier, une DLL et qu’elle doit descendre sur le réseau) lors du lancement. S’il existe des limitations réseau, FB1:</span><span class="sxs-lookup"><span data-stu-id="56893-356">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="56893-357">Réduisez le nombre de pannes de flux et de bande passante réseau utilisées lorsque vous lancez une application pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="56893-357">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="56893-358">Retardez le lancement jusqu’à ce que la totalité du FB1 ait été diffusée.</span><span class="sxs-lookup"><span data-stu-id="56893-358">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="56893-359">Le dysfonctionnement du flux réduit le temps de démarrage.</span><span class="sxs-lookup"><span data-stu-id="56893-359">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-360">Les packages d’application virtuelle pour lesquels FB1 est configuré doivent être à nouveau séquencés.</span><span class="sxs-lookup"><span data-stu-id="56893-360">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="56893-361">Suppression de FB1</span><span class="sxs-lookup"><span data-stu-id="56893-361">Removing FB1</span></span>

<span data-ttu-id="56893-362">La suppression de FB1 ne nécessite pas le programme d’installation d’application d’origine.</span><span class="sxs-lookup"><span data-stu-id="56893-362">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="56893-363">Après avoir suivi les étapes ci-dessous, il est recommandé de rétablir l’ordinateur qui exécute le Sequencer sur une capture instantanée saine.</span><span class="sxs-lookup"><span data-stu-id="56893-363">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="56893-364">**Interface utilisateur de Sequencer** -créez un nouveau package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="56893-364">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="56893-365">Suivez les étapes de la séquence pour personnaliser- &gt; streaming.</span><span class="sxs-lookup"><span data-stu-id="56893-365">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="56893-366">À l’étape de diffusion, ne sélectionnez pas **l’option optimiser le package de déploiement sur un réseau lent ou peu fiable**.</span><span class="sxs-lookup"><span data-stu-id="56893-366">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="56893-367">Le cas échéant, passez au **système d’exploitation cible**.</span><span class="sxs-lookup"><span data-stu-id="56893-367">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="56893-368">Modifier un package d’application virtuel existant</span><span class="sxs-lookup"><span data-stu-id="56893-368">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="56893-369">Effectuez les étapes de séquençage en continu.</span><span class="sxs-lookup"><span data-stu-id="56893-369">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="56893-370">Ne sélectionnez pas **l’option optimiser le package de déploiement sur un réseau lent ou non fiable**.</span><span class="sxs-lookup"><span data-stu-id="56893-370">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="56893-371">Accédez à **créer un package**.</span><span class="sxs-lookup"><span data-stu-id="56893-371">Move to **Create Package**.</span></span>

<span data-ttu-id="56893-372">**PowerShell** -mise à jour d’un package d’application virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="56893-372">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="56893-373">Ouvrez une session PowerShell avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="56893-373">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="56893-374">Import-module **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="56893-374">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="56893-375">**Update-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="56893-375">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="56893-376">"C:\\Packages\\MyPackage.appv"-programme d’installation</span><span class="sxs-lookup"><span data-stu-id="56893-376">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="56893-377">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="56893-377">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="56893-378">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="56893-378">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="56893-379">Remarque</span><span class="sxs-lookup"><span data-stu-id="56893-379">Note</span></span>**  
    <span data-ttu-id="56893-380">Cette applet de commande nécessite un exécutable (. exe) ou un fichier de commandes (. bat).</span><span class="sxs-lookup"><span data-stu-id="56893-380">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="56893-381">Vous devez fournir un exécutable vide ou un fichier de commandes.</span><span class="sxs-lookup"><span data-stu-id="56893-381">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56893-382">Étape</span><span class="sxs-lookup"><span data-stu-id="56893-382">Step</span></span></th>
<th align="left"><span data-ttu-id="56893-383">Concernant</span><span class="sxs-lookup"><span data-stu-id="56893-383">Considerations</span></span></th>
<th align="left"><span data-ttu-id="56893-384">Avantages</span><span class="sxs-lookup"><span data-stu-id="56893-384">Benefits</span></span></th>
<th align="left"><span data-ttu-id="56893-385">Compromis</span><span class="sxs-lookup"><span data-stu-id="56893-385">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56893-386">Aucune installation SXS lors de la publication</span><span class="sxs-lookup"><span data-stu-id="56893-386">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-387">Il n’est pas nécessaire de réorganiser les packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="56893-387">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="56893-388">Les assemblys SxS peuvent rester dans le package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="56893-388">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-389">Les dépendances d’assembly SxS ne sont pas installées au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="56893-389">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-390">Les dépendances d’assemblage SxS doivent être préinstallées.</span><span class="sxs-lookup"><span data-stu-id="56893-390">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="56893-391">Création d’un package d’application virtuelle sur le Sequencer</span><span class="sxs-lookup"><span data-stu-id="56893-391">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="56893-392">Si, au cours d’une analyse de Sequencer, un assemblage SxS (par exemple, un CV + + Runtime) est installé dans le cadre de l’installation d’une application, l’assemblage SxS est automatiquement détecté et inclus dans le package.</span><span class="sxs-lookup"><span data-stu-id="56893-392">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="56893-393">L’administrateur est alors averti et dispose de l’option d’exclusion de l’assembly SxS.</span><span class="sxs-lookup"><span data-stu-id="56893-393">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="56893-394">**Côté client**:</span><span class="sxs-lookup"><span data-stu-id="56893-394">**Client Side**:</span></span>

<span data-ttu-id="56893-395">Lors de la publication d’un package d’application virtuelle, le client App-V détectera si une dépendance à l’SxS requise est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="56893-395">When publishing a virtual application package, the App-V Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="56893-396">Si la dépendance n’est pas disponible sur l’ordinateur et qu’elle est incluse dans le package, un programme d’installation Windows traditionnel (.\*\* MSI\*\*) l’installation de l’assembly SxS sera lancée.</span><span class="sxs-lookup"><span data-stu-id="56893-396">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="56893-397">Comme nous l’avons mentionné précédemment, installez simplement la dépendance sur l’ordinateur exécutant le client pour vérifier que l’installation de Windows Installer (. msi) ne se produit pas.</span><span class="sxs-lookup"><span data-stu-id="56893-397">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56893-398">Étape</span><span class="sxs-lookup"><span data-stu-id="56893-398">Step</span></span></th>
<th align="left"><span data-ttu-id="56893-399">Concernant</span><span class="sxs-lookup"><span data-stu-id="56893-399">Considerations</span></span></th>
<th align="left"><span data-ttu-id="56893-400">Avantages</span><span class="sxs-lookup"><span data-stu-id="56893-400">Benefits</span></span></th>
<th align="left"><span data-ttu-id="56893-401">Compromis</span><span class="sxs-lookup"><span data-stu-id="56893-401">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56893-402">Utilisation sélective de fichiers de configuration dynamiques</span><span class="sxs-lookup"><span data-stu-id="56893-402">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-403">Le client App-V 5,1 doit analyser et traiter les fichiers de configuration dynamique suivants.</span><span class="sxs-lookup"><span data-stu-id="56893-403">The App-V 5.1 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="56893-404">Soyez conscient de la taille et de la complexité (exécution du script, inclusions ou exclusions VREG) du fichier.</span><span class="sxs-lookup"><span data-stu-id="56893-404">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="56893-405">De nombreux packages d’applications virtuelles peuvent avoir déjà des fichiers de configurations dynamiques spécifiques à un utilisateur ou à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="56893-405">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-406">Les durées de publication sont améliorées si ces fichiers sont utilisés de manière sélective ou pas du tout.</span><span class="sxs-lookup"><span data-stu-id="56893-406">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-407">Les packages d’applications virtuelles devront être reconfigurés individuellement ou via la console de gestion de l’application-V Server pour supprimer les fichiers de configuration dynamique associés.</span><span class="sxs-lookup"><span data-stu-id="56893-407">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="56893-408">Désactivation d’une configuration dynamique à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="56893-408">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="56893-409">Pour les packages déjà publiés, vous pouvez utiliser `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` sans</span><span class="sxs-lookup"><span data-stu-id="56893-409">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="56893-410">Paramètre **-DynamicDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="56893-410">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="56893-411">De même, lorsque vous ajoutez de nouveaux packages à l’aide de `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , n’utilisez pas le</span><span class="sxs-lookup"><span data-stu-id="56893-411">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="56893-412">Paramètre **-DynamicDeploymentConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="56893-412">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="56893-413">Pour obtenir des informations sur la façon d’appliquer une configuration dynamique, voir:</span><span class="sxs-lookup"><span data-stu-id="56893-413">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="56893-414">Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="56893-414">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

-   [<span data-ttu-id="56893-415">Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="56893-415">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="56893-416">Étape</span><span class="sxs-lookup"><span data-stu-id="56893-416">Step</span></span></th>
<th align="left"><span data-ttu-id="56893-417">Concernant</span><span class="sxs-lookup"><span data-stu-id="56893-417">Considerations</span></span></th>
<th align="left"><span data-ttu-id="56893-418">Avantages</span><span class="sxs-lookup"><span data-stu-id="56893-418">Benefits</span></span></th>
<th align="left"><span data-ttu-id="56893-419">Compromis</span><span class="sxs-lookup"><span data-stu-id="56893-419">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="56893-420">Compte d’exécution de script synchrone lors du cycle de vie du package.</span><span class="sxs-lookup"><span data-stu-id="56893-420">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-421">S’il est incorporé dans le package, l’ajout (PowerShell) peut être considérablement plus lent.</span><span class="sxs-lookup"><span data-stu-id="56893-421">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="56893-422">L’exécution de scripts lors du lancement d’une application virtuelle (StartVirtualEnvironment, StartProcess) et/ou ajout + publication aura un impact sur les performances perçues lors d’une ou plusieurs de ces opérations de cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="56893-422">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-423">L’utilisation de scripts asynchrones (sans blocage) permet de garantir que les opérations de cycle de vie s’exécutent efficacement.</span><span class="sxs-lookup"><span data-stu-id="56893-423">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-424">Cette étape nécessite une connaissance du fonctionnement de tous les packages d’applications virtuelles incluant des brochures de script intégrées, qui disposent de fichiers de configurations dynamiques associés et de références et d’exécution des scripts de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="56893-424">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="56893-425">Supprimer les polices virtuelles superflues du package.</span><span class="sxs-lookup"><span data-stu-id="56893-425">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-426">La plupart des applications examinées par l’équipe de produit App-V contenaient un petit nombre de polices, généralement moins de 20.</span><span class="sxs-lookup"><span data-stu-id="56893-426">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-427">Les polices virtuelles influent sur les performances de la publication.</span><span class="sxs-lookup"><span data-stu-id="56893-427">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="56893-428">Les polices souhaitées devront être activées ou installées en mode natif.</span><span class="sxs-lookup"><span data-stu-id="56893-428">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="56893-429">Pour obtenir des instructions, voir installer ou désinstaller des polices.</span><span class="sxs-lookup"><span data-stu-id="56893-429">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="56893-430">Identifier les polices virtuelles qui existent dans le package</span><span class="sxs-lookup"><span data-stu-id="56893-430">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="56893-431">Effectuez une copie du package.</span><span class="sxs-lookup"><span data-stu-id="56893-431">Make a copy of the package.</span></span>

-   <span data-ttu-id="56893-432">Renommer le package \ _copy. AppV en Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="56893-432">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="56893-433">Ouvrez AppxManifest.xml et recherchez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="56893-433">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="56893-434">&lt;AppV: extension category = "AppV. polices"&gt;</span><span class="sxs-lookup"><span data-stu-id="56893-434">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="56893-435">&lt;AppV: polices&gt;</span><span class="sxs-lookup"><span data-stu-id="56893-435">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="56893-436">&lt;AppV: chemin de police = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /AppV: font&gt;</span><span class="sxs-lookup"><span data-stu-id="56893-436">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="56893-437">Remarque</span><span class="sxs-lookup"><span data-stu-id="56893-437">Note</span></span>**  
    <span data-ttu-id="56893-438">S’il existe des polices marquées comme **DelayLoad**, celles-ci n’ont aucun impact sur le premier lancement.</span><span class="sxs-lookup"><span data-stu-id="56893-438">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="56893-439">Exclusion de polices virtuelles du package</span><span class="sxs-lookup"><span data-stu-id="56893-439">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="56893-440">Utilisez le fichier de configuration dynamique qui correspond le mieux à la configuration de déploiement pour tous les utilisateurs sur un ordinateur, configuration utilisateur pour des utilisateurs ou des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="56893-440">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="56893-441">Désactiver les polices avec le déploiement ou la configuration de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-441">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="56893-442">Polices</span><span class="sxs-lookup"><span data-stu-id="56893-442">Fonts</span></span>

--&gt;

<span data-ttu-id="56893-443">&lt;Polices activées = "faux"/&gt;</span><span class="sxs-lookup"><span data-stu-id="56893-443">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="56893-444">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="56893-444">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="56893-445">Terminologie des recommandations en matière de performances de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="56893-445">App-V 5.1 Performance Guidance Terminology</span></span>


<span data-ttu-id="56893-446">Les termes suivants sont utilisés lors de la description des concepts et actions liés à l’optimisation des performances d’App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="56893-446">The following terms are used when describing concepts and actions related to App-V 5.1 performance optimization.</span></span>

-   <span data-ttu-id="56893-447">**Complexité** : désigne l’une ou plusieurs caractéristiques de package susceptibles d’avoir un impact sur les performances lors de la préconfiguration (**Add-AppvClientPackage**) ou de l’intégration (**publication-AppvClientPackage**).</span><span class="sxs-lookup"><span data-stu-id="56893-447">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="56893-448">Voici quelques exemples de caractéristiques: taille du manifeste, nombre de polices virtuelles, nombre de fichiers.</span><span class="sxs-lookup"><span data-stu-id="56893-448">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="56893-449">**Désintégration** : supprime les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-449">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="56893-450">**Nouvelle intégration** : applique les intégrations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56893-450">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="56893-451">**Non permanent, en regroupement** : crée un ordinateur exécutant un environnement virtuel chaque fois qu’il se connecte.</span><span class="sxs-lookup"><span data-stu-id="56893-451">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="56893-452">**Permanent et personnel** : ordinateur exécutant un environnement virtuel qui reste le même pour chaque connexion.</span><span class="sxs-lookup"><span data-stu-id="56893-452">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="56893-453">**État** -pour ce document, ce qui signifie que les intégrations des utilisateurs sont conservées entre les sessions et qu’une technologie de gestion de l’environnement utilisateur est utilisée en conjonction avec un hôte de session hôte ou VDI non persistant.</span><span class="sxs-lookup"><span data-stu-id="56893-453">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="56893-454">**Sans état** – représente un scénario dans lequel aucun état utilisateur n’est persistant entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="56893-454">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="56893-455">**Déclencheur** (déclencheur d’action natif).</span><span class="sxs-lookup"><span data-stu-id="56893-455">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="56893-456">UPM utilise ces types de déclencheurs pour lancer des opérations de surveillance ou de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="56893-456">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="56893-457">**Interface utilisateur** : dans le contexte de App-V 5,1, l’interface utilisateur, quantitativement, est la somme des parties suivantes:</span><span class="sxs-lookup"><span data-stu-id="56893-457">**User Experience** - In the context of App-V 5.1, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="56893-458">À partir du moment où les utilisateurs ouvrent une session pour pouvoir manipuler le bureau.</span><span class="sxs-lookup"><span data-stu-id="56893-458">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="56893-459">À partir du moment où le Bureau peut être utilisé pour une actualisation de publication (dans les termes de PowerShell, la synchronisation) lors de l’utilisation de l’infrastructure serveur complète App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="56893-459">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.1 full server infrastructure.</span></span> <span data-ttu-id="56893-460">Dans les instances autonomes, il s’agit du moment où les commandes PowerShell **Add-AppVClientPackage** et **Publish-AppVClientPackage** sont initialisées.</span><span class="sxs-lookup"><span data-stu-id="56893-460">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="56893-461">Du début à la fin de l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="56893-461">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="56893-462">Dans les instances autonomes, il s’agit de la première à la dernière application virtuelle publiée.</span><span class="sxs-lookup"><span data-stu-id="56893-462">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="56893-463">À partir du moment où l’application virtuelle est disponible pour le lancement à partir d’un raccourci.</span><span class="sxs-lookup"><span data-stu-id="56893-463">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="56893-464">Par ailleurs, il s’agit de l’emplacement d’enregistrement de l’Association de type de fichier et lancera une application virtuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="56893-464">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="56893-465">**Gestion des profils utilisateur** : l’approche contrôlée et structurée pour gérer les composants utilisateur associés à l’environnement.</span><span class="sxs-lookup"><span data-stu-id="56893-465">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="56893-466">Par exemple, profils utilisateur, gestion des préférences et de la stratégie, contrôle d’application et déploiement d’application.</span><span class="sxs-lookup"><span data-stu-id="56893-466">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="56893-467">Vous pouvez utiliser la création de scripts ou des solutions tierces pour configurer l’environnement selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="56893-467">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="56893-468">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56893-468">Related topics</span></span>


[<span data-ttu-id="56893-469">Guide de l’administrateur de Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="56893-469">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)









